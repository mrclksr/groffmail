### About
*groffmail* is a filter script that beautifies your emails using *groff*.

### Usage
	groffmail [-l <line length>] [--] [<groff options>]
### Example
#### Input

	> Lorem ipsum dolor sit amet, consetetur sadipscing elitr,  sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
	>> Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
	> Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.
	
	Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.
	
	.IP \(bu
	Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis.
	.IP \(bu
	At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr,  sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua.
	.LP
	.B1
	.ce
	Lorem Ipsum
	.LP
	At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr,  At accusam aliquyam diam diam dolore dolores duo eirmod eos erat, et nonumy sed tempor et et invidunt justo labore Stet clita ea et gubergren, kasd magna no rebum. sanctus sea sed takimata ut vero voluptua. est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr,  sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
	.B2
	.LP
	Consetetur sadipscing elitr,  sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. [\**]
	At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. [\**]
	
	.FS
	First footnote
	.FE
	.FS
	Second footnote
	.FE
	
#### Output
	$ ./groffmail -l65 -- -ms -Tutf8 < input.txt
	> Lorem  ipsum  dolor sit amet, consetetur sadipscing elitr,  sed
	> diam nonumy eirmod tempor invidunt ut labore  et  dolore  magna
	> aliquyam  erat,  sed  diam  voluptua. At vero eos et accusam et
	> justo duo dolores et ea rebum. Stet clita  kasd  gubergren,  no
	> sea takimata sanctus est Lorem ipsum dolor sit amet.
	>> Duis  autem  vel  eum  iriure  dolor in hendrerit in vulputate
	>> velit esse molestie consequat, vel  illum  dolore  eu  feugiat
	>> nulla facilisis at vero eros et accumsan et iusto odio dignis‐
	>> sim qui blandit praesent luptatum zzril delenit augue duis do‐
	>> lore  te  feugait  nulla facilisi. Lorem ipsum dolor sit amet,
	>> consectetuer adipiscing elit, sed diam  nonummy  nibh  euismod
	>> tincidunt ut laoreet dolore magna aliquam erat volutpat.
	> Ut wisi enim ad minim veniam, quis nostrud exerci tation ullam‐
	> corper suscipit lobortis nisl ut aliquip ex ea  commodo  conse‐
	> quat. Duis autem vel eum iriure dolor in hendrerit in vulputate
	> velit esse molestie consequat,  vel  illum  dolore  eu  feugiat
	> nulla  facilisis at vero eros et accumsan et iusto odio dignis‐
	> sim qui blandit praesent luptatum zzril delenit augue duis  do‐
	> lore te feugait nulla facilisi.
	
	Nam  liber  tempor  cum soluta nobis eleifend option congue nihil
	imperdiet doming id quod mazim placerat facer possim assum. Lorem
	ipsum dolor sit amet, consectetuer adipiscing elit, sed diam non‐
	ummy nibh euismod tincidunt ut laoreet dolore magna aliquam  erat
	volutpat.  Ut  wisi  enim  ad  minim  veniam, quis nostrud exerci
	tation ullamcorper suscipit lobortis nisl ut aliquip ex  ea  com‐
	modo consequat.
	
	
	•    Duis  autem  vel  eum iriure dolor in hendrerit in vulputate
	     velit esse molestie consequat, vel illum dolore  eu  feugiat
	     nulla facilisis.
	
	•    At  vero  eos  et  accusam et justo duo dolores et ea rebum.
	     Stet clita kasd gubergren, no sea takimata sanctus est Lorem
	     ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur
	     sadipscing elitr,  sed diam nonumy eirmod tempor invidunt ut
	     labore et dolore magna aliquyam erat, sed diam voluptua.
	
	┌───────────────────────────────────────────────────────────────┐
	│                          Lorem Ipsum                          │
	│                                                               │
	│At  vero  eos et accusam et justo duo dolores et ea rebum. Stet│
	│clita kasd gubergren, no sea takimata sanctus est  Lorem  ipsum│
	│dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipsc‐│
	│ing elitr,  At accusam aliquyam diam diam  dolore  dolores  duo│
	│eirmod  eos erat, et nonumy sed tempor et et invidunt justo la‐│
	│bore Stet clita ea et gubergren, kasd magna no  rebum.  sanctus│
	│sea  sed  takimata  ut vero voluptua. est Lorem ipsum dolor sit│
	│amet. Lorem ipsum dolor sit amet, consetetur sadipscing  elitr,│
	│sed  diam  nonumy  eirmod  tempor  invidunt ut labore et dolore│
	│magna aliquyam erat.                                           │
	└───────────────────────────────────────────────────────────────┘
	
	Consetetur sadipscing elitr,  sed‐diam nonumy eirmod  tempor  in‐
	vidunt  ut  labore et dolore magna aliquyam erat, sed diam volup‐
	tua. [1] At vero eos et accusam et justo duo dolores et ea rebum.
	Stet  clita kasd gubergren, no sea takimata sanctus est Lorem ip‐
	sum dolor sit amet. [2]
	
	
	
	
	───────────
	1 First footnote
	2 Second footnote
	
	
