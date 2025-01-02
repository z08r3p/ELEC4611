java c
ELEC4611 POWER SYSTEM EQUIPMENT LABORATORY
EXPERIMENT 5
COMPUTER-BASED ANALYSIS OF ELECTRIC STRESS
1.                  INTRODUCTIONInsulating   materials   used   in   power   system   equipment   are   subjected   to   severe   electric   stress.   Breakdown   will   occur   if the   stress   exceeds   the   material   breakdown   strength.   Knowledge   of   the    electric    field      distribution      in      a      given      insulating       structure    is      important      as      it      enables   determination   of the permissible   operating   voltage   and   methods   of controlling   electric   stress.   This knowledge   can be   achieved using   computer-based numerical   methods   such   as   the   Finite   Element    Method    (FEM)    to      solve      the      Laplace’s      or      Poisson’s      field      equations.      Note      that   practical   insulating   systems   usually   involve   a   combination   of   different   insulating   materials   with   different   permittivity   and   also   require   solving   three-dimensional   fields   with   complex   boundary conditions.
2.                  EXPERIMENTThis      experiment    involves    the      use      of    computer      programs.       There      are    many      commercial   software   programs   for   field   analysis.   One   such   product   is   the   Ansys   Maxwell   2D   for   two-   dimensional   field   analysis   (www.ansys.com).   The   workflow process   to   solve   a   field problem   involves   six   steps:   create   a   structure   →   assign materials   →   add boundaries   →   add   excitations   → setup   the   solution   →   solve   → post   processing.
(a)             Draw,   set   up,   and   solve   for the   electrostatic   field   in between   two parallel   copper   plates   (1 mm thickness,   15 mm   length)   at   5 mm   apart   with   an   applied   voltage   of   1   kV.   Verify   that the electric field   is uniform.
         Starting Maxwell: do one of   the   following:
-          Double-click   the   ANASYS   Electronics   Desktop   icon   on   Windows   Desktop.
-          Use   Start   menu   to   select   Programs>ANASYS   Electronics   Desktop
         Create a 2D   Project:
-            From   the   toolbar   Maxwell>Maxwell   2D
The Project Manager window will appear on the left.   To create solution type, do   one of   the   followings:
-            Choose Maxwell 2D>Solution   Type>Electrostatic
-          Right click   on Maxwell2Ddesign1 in   Project   Manager window,   then   choose Solution   Type and Electrostatic.
Note: You need to set the Solution   Type   to Electrostatic   when you insert a new   project.
         Create modeling objects:
In order to draw the above structure (parallel plates),   you   can   follow   these   steps:   (a) Design the first plate:
-            Draw>Line
-            In status bar, enter 0   in X   box   and   0   in   Y   box.
-            Change the coordinate from Absolute to Relative.
-          Enter 0   in   dX   box   and   1   in   dY box   (after   this   step,   you   can   see   a   vertical   line   with   length   of   1mm   will   be   drawn).
-            Enter   15 in dX box and   0   in   dY   box.
-            Enter 0 in dX box   and   -1   in   dY box.
-            Enter -15 in dX box   and   0   in   dY box.
-          Right click   on   design window>Done.   After this   step,   the   object   will be   automatically   named   Polyline1.
(b) Design the second plate:
-          Repeat part   (a) above   with   appropriate   coordination   start   with   0   in   X   box   and   6   in Y box.
-            The plate will be automatically named Polyline2.
(c) Design boundary:
-            Draw>Rectangle
-            In status bar, enter -20 in   X box   and   27   in   Y box.
-            Enter 55 in dX box   and   -47   in   dY box
-            It will be named Rectangle1
      Defining Materials:
In this step, the materials as well as their characteristics   will be   assigned   to   above   created objects.
Choose Polyline1 and Polyline2 objects   > Modeler >   Assign Material. In materials   tab, choose copper   >   OK.
         Setup   Boundaries   and   Excitation:
(a)      Choose Polyline1>Maxwell 2D>Excitation>Assign>Voltage>enter 1000   V>OK
(b)      Choose Polyline2>Maxwell 2D>Excitation>Assign>Voltage>enter 0   V>OK
(c)      Edit>Selection Mode>Edges.
Hold Ctrl + left click on   4   edges   of   Rectangle1
>Maxwell 2D>Boundaries>Assign>Balloon>OK.
         Generating a   Solution
(a)      Setup   a   Matrix   Calculation: Maxwell   2D>Parameters>Assign>Matrix>Check Voltage   1 as Signal   Line and   Voltage 2 as   Ground.
(b)      Setup   a   Solution: Maxwell   2D>Analysis   Setup>Add   Solution   Setup>Leave these criteria as   default.
         Checking Validity and Run   Simulation:
(a)      Maxwell 2D>   Validation Check Make sure all steps are   checked.   (b)    Run   simulation: Maxwell   2D>Analyze   All.
         Monitoring electric stress:
Choose Rectangle1   >Maxwell 2D>Fields>Fields>Mag_E>AllObjects
(b)            Consider a right-angled structure as shown   in   Figure   1:
            Create a new Maxwell 2D project and obtain the field plot   for this   structure.
            Comment   of   the   results.
            Suggest   a minor modification that   can be   done   to   the   structure   to   reduce   the   stress.   Redo the plot to verify.
Note   that:
            Properly set the   solution type.
            When   designing boundary,   create   a   rectangle   that   is   relatively   large   in   order   to   see   the complete field   distribution.
            When      drawing      the      object,      choose      an      origin      by      yourself    (or       following       the   instructions   of your   lab   demo)   and   work   out   the relative   coordinates   for the   rest   of   points.
            Choose Modeler >Units>cm

Figure   1


Note:   The   thickness   of the   above   electrodes   is   1cm,   and   the   distance between   two   electrodes   is   5cm.
(c)             A   cable,   shown   in   Figure   2,   has   an   eccentric   core   and   axia代 写ELEC4611 POWER SYSTEM EQUIPMENT LABORATORY EXPERIMENT 5
代做程序编程语言l   uniformity.   There   are    100   kilo-volts   across   the   cable   and   the   insulation   has   a   relative   permittivity   εr      = 2.0 and   resistivity    P   = 1013          Ωm    (conductivity    can      be      worked      out      by      taking      the      inverse      of   resistivity).   The   geometrical   parameters   can   be   determined   using   the   scale   provided   in   Fig.   2.
            Obtain the field plot for this cable using Maxwell   2D.
            Determine   the   stress   and   voltage   at   points   P1    and   P2.   Compare   simulation   results   with   those   obtained   using   manual   field   mapping   (see   Appendix).
            Identify   the   region   of   highest   stress   and   determine   its   value.
            Calculate the cable capacitance and insulation resistance (per unit length).
            Explain   why   the   lower   half   plot   (in   Fig.2) is   incorrect.
            If   this   cable   is   concentric, redo the   field plot   and   determine the   highest   stress.   This   case can also be solved analytically and the   electric   field   at   a   radius   r   is   given by:

where   b   is   the   outer   radius, a   is   the   inner   radius,   and   Vis   the   total   voltage   across   the
insulation. Compare the results. Also, compare against that of   the eccentric   core.       Note: inner circle (cable core) should be   subtracted in   order to   achieve   accurate   result.

Fig.2:   (a)   curvilinear   squares   plot   for   an   eccentric   cable   of constant   cross-   section,   (b)   general   curvilinear   square   and   its   subdivisions,   (c)   expanded   view   of   curvilinear   square   2   that   forms   the   ends   of   a   curvilinear   cell   of   depth   d   (m).
(d)          In      many      high      voltage      insulation      systems      multi-dielectric      structures      are      used      with   dielectric   materials   with   different   relative   permittivity   in   order   to   provide   better   use   of   insulation    by    reducing    the    overall    insulation    thickness      and      making      the      field      more uniform   within   the   overall   layer   structure.   In   other   cases,   the   use   of   multi-dielectric   structures   is   unavoidable   such   as   in   a   HV   bushing   where   the   small   gap   between   the   porcelain   insulator   and   the   inner   HV   conductor   is   normally   filled   with   insulating   oil.   Consider   the    11    kV    model    bushing    as    specified    in    Experiment      3    with    the      applied   voltage   of   20 kV.
            Obtain   the   field   plot   for   the   case   when   the   gap   is   air,   and   determine   the   highest   stress   by   modelling   cross   section   of   bushing
            Obtain the field plot when the gap is   filled with   oil,   and   determine the   highest   stress   by   modelling   cross   section   of   bushing
            Comment on the results.
3.                  REFERENCES
1.       E. Kuffel, W.S. Zaengl,   and   J.   Kuffel, High    Voltage Engineering: Fundamentals,   2nd   ed., Butterworth-Heinemann, 2000.
2.       Ansoft      Corporation,      Getting      Started:    A      2D      Electrostatic      Problem,      Maxwell      2D Student Version, 2002.


4.                APPENDIX   - FIELD   ANALYSIS   BY   MANUAL   FIELD   MAPPING
To   solve   a   field   problem,   we   need   to   obtain   the   flux   or   potential   distribution.   From   this,   we   can obtain the required macroscopic and microscopic   properties   
e.g.      R, C, L   ,      J   ,   D   ,   B   ,   E   , etc
There are three methods of   obtaining flux and potential distribution:
1.                Solve Laplace’s equation    (   ▽2φ=   0) or Poisson’s equation    (   ▽2φ=   −Pε)   analytically or numerically
2.                Manual field mapping
3.               Numerical iteration
Field mapping
This   technique   uses   known   field   properties   to   draw   up   a   map   of   the   field   for   a   particular   configuration. It can give surprisingly   accurate results.
Field properties:
(i)                      Flux lines and   equi-potentials   are   orthogonal
(ii)                   Surfaces of   flux   sources   are   equi-potentials
(iii)                Flux lines intersect sources and   sinks   orthogonally.   
The aim is to divide the field structure   into   curvilinear   squares   (assuming   there   is   symmetry   in   the third dimension)

If the element is part of current flow and the current density is J, and electric field E


ΔI = J    ×   area = J   ×   (   Δx   )   = JΔx            (   =1 m)
ΔV   =   EΔy
Hence, resistance   of   the   elemental   section   is:


   = P      if      = 1m    and    Δy = Δx
Thus,    each   curvilinear    square   of   unit    depth   has   resistance   P.   The   total   resistance   can   be   obtained by counting squares in the   full map.
This holds for any   field, the only difference being the property relative to   the   field   type,   e.g.
            For   an   electric   field, capacitance   of   the   unit   square      =   ε
            For   a   magnetic   field, the   unit   square   inductance      =   μ
            For a thermal field, the unit square conductance    = k
e.g.   for   a   current   flow   field   above,   if   there   are   n   equipotential   drops   and   m   flux   tubes   of   current and the resistivity is P, then the total R is:
    ohms
In the above:   n = 4, m = 8            →       R =     ohms       
If   a   capacitance:
ΔΨ = ΔQ    and    total   Q   = mΔQ = 8ΔQ Δφ   = ΔV      and      total   V   = nΔV = 4ΔV
Hence:
For   flux   density   and   potential   gradient,   use   the   appropriate   single   square   and   the   applicable   scale   factor   of   the   map:
Flux density = 
ΔΨ            Ψm
=                     =
Δx                     Δx
Thus   if we   know   total   Ψ   and   φ   and   get   m   and   n,   and   Δx    (=Δy   ) from   the   map,   we   can   find   ΔΨΔx      and      Δφ Δy   .
   
   

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
