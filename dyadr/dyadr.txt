# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Dyadic data analysis Use dyadr With (In) R Software
install.packages("remotes")
remotes::install_github("RandiLGarcia/dyadr")
library("nlme")
library("dyadr")
# Estimation Dyadic data analysis Use dyadr With (In) R Software
dyadr = read.csv("https://raw.githubusercontent.com/timbulwidodostp/dyadr/main/dyadr/dyadr.csv",sep = ";")
dyadr <- gls(Satisfaction_A ~ Tension_A + Tension_P + SelfPos_A + SelfPos_P, na.action = na.omit, correlation = corCompSymm(form = ~ 1 | CoupleID), data = dyadr)
smallsummary(dyadr)
# Dyadic data analysis Use dyadr With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished