# 👻 Ghost ደህንነት ሞጁል
**በPowerShell ላይ የተመሰረተ Windows እና Azure ደህንነት ማጠናከሪያ መሳሪያ**

> **ለWindows ተርሚናል ነጥቦች እና Azure አካባቢዎች ቅድመ-ንቁ ደህንነት ማጠናከሪያ።** Ghost አላስፈላጊ አገልግሎቶችን እና ፕሮቶኮሎችን በማሰናከል የተለመዱ የጥቃት ቬክተሮችን ለመቀነስ የሚረዱ በPowerShell ላይ የተመሰረቱ ማጠናከሪያ ተግባራትን ይሰጣል።

## ⚠️ አስፈላጊ ማስተዋወቂያዎች

**ፈተና ያስፈልጋል**: ሁሌም Ghost-ን በምርት-ያልሆኑ አካባቢዎች ውስጥ መጀመሪያ ይፈትኑ። አገልግሎቶችን ማሰናከል ህጋዊ የንግድ ተግባራትን ሊጎዳ ይችላል።

**ምንም ዋስትና የለም**: Ghost የተለመዱ የጥቃት ቬክተሮችን ቢያነጣጥርም, ምንም የደህንነት መሳሪያ ሁሉንም ጥቃቶች መከላከል አይችልም። ይህ የአጠቃላይ የደህንነት ስትራቴጂ አንድ አካል ነው።

**የአሠራር ተጽእኖ**: አንዳንድ ተግባራት የስርዓት ተግባርን ሊጎዱ ይችላሉ። ከማሰማራት በፊት እያንዳንዱን ቅንብር በጥንቃቄ ይገምግሙ።

**ሙያዊ ግምገማ**: ለምርት አካባቢዎች, ቅንብሮች ከድርጅትዎ ፍላጎቶች ጋር እንዲጣጣሙ ለማረጋገጥ ከደህንነት ባለሙያዎች ጋር ይማከሩ።

## 📊 የደህንነት መልክዓ ምድር

የRansomware ጉዳቶች **በ2025 $57 ቢሊዮን** ደርሰዋል፣ ብዙ ስኬታማ ጥቃቶች መሰረታዊ Windows አገልግሎቶችን እና ስህተተኛ ውቅሮችን እንደሚጠቀሙ የሚያሳዩ ምርምሮች አሉ። የተለመዱ የጥቃት ቬክተሮች የሚከተሉትን ያካትታሉ:

- **የ90% ransomware ሁኔታዎች** RDP መበዝበዝን ያካትታሉ
- **SMBv1 ድክመቶች** እንደ WannaCry እና NotPetya ያሉ ጥቃቶችን አስችለዋል
- **የሰነድ ማክሮዎች** ዋና የmalware ማድረስ ዘዴ ሆነው ይቀራሉ
- **በUSB ላይ የተመሰረቱ ጥቃቶች** ከአየር የተነጠሉ አውታረ መረቦችን ማነጣጠር ይቀጥላሉ
- **የPowerShell አላግባብ መጠቀም** በቅርብ ዓመታት በሚያስደንቅ ሁኔታ ጨምሯል

## 🛡️ Ghost ደህንነት ተግባራት

Ghost **16 Windows ማጠናከሪያ ተግባራት** እና **Azure ደህንነት ውህደት** ይሰጣል:

### የWindows ተርሚናል ነጥብ ማጠናከሪያ

| ተግባር | ዓላማ | ግምት |
|-------|------|------|
| `Set-RDP` | Remote Desktop መዳረሻን ያስተዳድራል | በርቀት አስተዳደርን ሊጎዳ ይችላል |
| `Set-SMBv1` | legacy SMB ፕሮቶኮልን ይቆጣጠራል | ለጣሊያን አሮጌ ስርዓቶች ያስፈልጋል |
| `Set-AutoRun` | AutoPlay/AutoRun ን ይቆጣጠራል | የተጠቃሚ ምቹነትን ሊጎዳ ይችላል |
| `Set-USBStorage` | USB ማከማቻ መሳሪያዎችን ይገድባል | ህጋዊ USB አጠቃቀምን ሊጎዳ ይችላል |
| `Set-Macros` | የOffice ማክሮ ትግበራን ይቆጣጠራል | በማክሮ የነቁ ሰነዶችን ሊጎዳ ይችላል |
| `Set-PSRemoting` | PowerShell remotingን ያስተዳድራል | በርቀት አስተዳደርን ሊጎዳ ይችላል |
| `Set-WinRM` | Windows Remote Management ን ይቆጣጠራል | በርቀት አስተዳደርን ሊጎዳ ይችላል |
| `Set-LLMNR` | የስም ውሳኔ ፕሮቶኮልን ያስተዳድራል | አብዛኛውን ጊዜ ለማሰናከል ደህንነቱ የተጠበቀ ነው |
| `Set-NetBIOS` | NetBIOS over TCP/IP ን ይቆጣጠራል | legacy መተግበሪያዎችን ሊጎዳ ይችላል |
| `Set-AdminShares` | አስተዳደራዊ ማጋሪያዎችን ያስተዳድራል | በርቀት ፋይል መዳረሻን ሊጎዳ ይችላል |
| `Set-Telemetry` | የውሂብ ስብሰባን ይቆጣጠራል | የመመርመሪያ ችሎታዎችን ሊጎዳ ይችላል |
| `Set-GuestAccount` | Guest መለያን ያስተዳድራል | አብዛኛውን ጊዜ ለማሰናከል ደህንነቱ የተጠበቀ ነው |
| `Set-ICMP` | ping ምላሾችን ይቆጣጠራል | የአውታረ መረብ መመርመሪያን ሊጎዳ ይችላል |
| `Set-RemoteAssistance` | Remote Assistance ን ያስተዳድራል | የእርዳታ ዴስክ ስራዎችን ሊጎዳ ይችላል |
| `Set-NetworkDiscovery` | የአውታረ መረብ ግኝትን ይቆጣጠራል | የአውታረ መረብ ዳሰሳን ሊጎዳ ይችላል |
| `Set-Firewall` | Windows Firewall ን ያስተዳድራል | ለአውታረ መረብ ደህንነት ወሳኝ ነው |

### Azure Cloud ደህንነት

| ተግባር | ዓላማ | መስፈርቶች |
|-------|------|-----------|
| `Set-AzureSecurityDefaults` | መሰረታዊ Azure AD ደህንነትን ያንቃል | Microsoft Graph ፈቃዶች |
| `Set-AzureConditionalAccess` | የመዳረሻ ፖሊሲዎችን ያዋቅራል | Azure AD P1/P2 ፍቃድ |
| `Set-AzurePrivilegedUsers` | ልዩ መብት ያላቸውን ሒሳቦች ይመረምራል | Global Admin ፈቃዶች |

### የድርጅት ማሰማራት አማራጮች

| ዘዴ | የአጠቃቀም ጉዳይ | መስፈርቶች |
|-----|---------------|-----------|
| **ቀጥተኛ አፈጻጸም** | ፈተና፣ ትናንሽ አካባቢዎች | የአካባቢ አስተዳዳሪ መብቶች |
| **Group Policy** | የዶሜይን አካባቢዎች | ዶሜይን አስተዳዳሪ፣ GP አስተዳደር |
| **Microsoft Intune** | cloud-የሚተዳደሩ መሳሪያዎች | Intune ፍቃድ፣ Graph API |

## 🚀 ፈጣን መጀመሪያ

### የደህንነት ግምገማ
```powershell
# Ghost ሞጁልን ጫን
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# የአሁኑን የደህንነት አቋም ይፈትሹ
Get-Ghost
```

### መሰረታዊ ማጠናከሪያ (መጀመሪያ ይፈትኑ)
```powershell
# አስፈላጊ ማጠናከሪያ - በላቦራቶሪ አካባቢ ውስጥ መጀመሪያ ይፈትኑ
Set-Ghost -SMBv1 -AutoRun -Macros

# ለውጦችን ይገምግሙ
Get-Ghost
```

### የድርጅት ማሰማራት
```powershell
# Group Policy ማሰማራት (የዶሜይን አካባቢዎች)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Intune ማሰማራት (cloud-የሚተዳደሩ መሳሪያዎች)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 የመትከያ ዘዴዎች

### አማራጭ 1: ቀጥተኛ አውራድ (ፈተና)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### አማራጭ 2: ሞጁል መትከያ
```powershell
# ከPowerShell Gallery ይጫኑ (ሲቻል)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### አማራጭ 3: የድርጅት ማሰማራት
```powershell
# ለGroup Policy ማሰማራት ወደ አውታረ መረብ ቦታ ኮፒ ያድርጉ
# ለcloud ማሰማራት Intune PowerShell ስክሪፕቶችን ያዋቅሩ
```

## 💼 የአጠቃቀም ጉዳይ ምሳሌዎች

### ትንሽ ንግድ
```powershell
# ዝቅተኛ ተጽእኖ ያለው መሰረታዊ ጥበቃ
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### የጤና እንክብካቤ አካባቢ
```powershell
# HIPAA ላይ ያተኮረ ማጠናከሪያ
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### የገንዘብ አገልግሎቶች
```powershell
# የከፍተኛ ደህንነት ውቅር
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Cloud-First ድርጅት
```powershell
# Intune-የሚተዳደር ማሰማራት
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 የተግባር ዝርዝሮች

### ዋና ማጠናከሪያ ተግባራት

#### የአውታረ መረብ አገልግሎቶች
- **RDP**: remote desktop መዳረሻን ይዘጋል ወይም ወደብን ያሰራሳል
- **SMBv1**: legacy ፋይል ማጋሪያ ፕሮቶኮልን ያሰናክላል
- **ICMP**: ለአሰሳ ping ምላሾችን ይከላከላል
- **LLMNR/NetBIOS**: legacy ስም ውሳኔ ፕሮቶኮሎችን ይዘጋል

#### የመተግበሪያ ደህንነት
- **ማክሮዎች**: በOffice መተግበሪያዎች ውስጥ የማክሮ አፈጻጸምን ያሰናክላል
- **AutoRun**: ከማስወገጃ ሚዲያ ራስ-ሰር አፈጻጸምን ይከላከላል

#### የርቀት አስተዳደር
- **PSRemoting**: PowerShell ርቀት ክፍለ ጊዜዎችን ያሰናክላል
- **WinRM**: Windows Remote Management ን ያቆማል
- **Remote Assistance**: የርቀት እርዳታ ግንኙነቶችን ይዘጋል

#### የመዳረሻ ቁጥጥር
- **Admin Shares**: C$፣ ADMIN$ ማጋሪያዎችን ያሰናክላል
- **Guest Account**: የGuest መለያ መዳረሻን ያሰናክላል
- **USB Storage**: የUSB መሳሪያ አጠቃቀምን ይገድባል

### Azure ውህደት
```powershell
# ከAzure tenant ጋር ተገናኝ
Connect-AzureGhost -Interactive

# የደህንነት ነባሮችን አንቃ
Set-AzureSecurityDefaults -Enable

# ሁኔታዊ መዳረሻን ያዋቅሩ
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# ልዩ መብት ያላቸውን ተጠቃሚዎች ይመርምሩ
Set-AzurePrivilegedUsers -AuditOnly
```

### Intune ውህደት (በv2 ውስጥ አዲስ)
```powershell
# ከIntune ጋር ተገናኝ
Connect-IntuneGhost -Interactive

# በIntune ፖሊሲዎች በኩል ማሰማራት
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ አስፈላጊ ግምቶች

### የፈተና መስፈርቶች
- **የላቦራቶሪ አካባቢ**: ሁሉንም ቅንብሮች በተለየ አካባቢ ውስጥ መጀመሪያ ይፈትኑ
- **ደረጃ በደረጃ ማሰማራት**: ችግሮችን ለመለየት ቀስ በቀስ ይሰማሩ
- **የመመለስ እቅድ**: ሲፈልጉ ለውጦችን መመለስ እንደሚችሉ ያረጋግጡ
- **ሰነድ**: ለአካባቢዎ የሚሰሩ ቅንብሮችን ይመዝግቡ

### የሊሆን ተጽእኖ
- **የተጠቃሚ ምርታማነት**: አንዳንድ ቅንብሮች ዕለታዊ የሥራ ፍሰትን ሊጎዱ ይችላሉ
- **Legacy መተግበሪያዎች**: አሮጌ ስርዓቶች የተወሰኑ ፕሮቶኮሎችን ሊፈልጉ ይችላሉ
- **የርቀት መዳረሻ**: በህጋዊ የርቀት አስተዳደር ላይ ያለውን ተጽእኖ ግምት ውስጥ ያስገቡ
- **የንግድ ሂደቶች**: ቅንብሮች ወሳኝ ተግባራትን እንደማይሰብሩ ያረጋግጡ

### የደህንነት ውስንነቶች
- **በጥልቀት መከላከል**: Ghost አንድ የደህንነት ሽፋን ነው፣ ሙሉ መፍትሄ አይደለም
- **ቀጣይ አስተዳደር**: ደህንነት ቀጣይነት ያለው ክትትልና ዝማኔዎችን ይፈልጋል
- **የተጠቃሚ ስልጠና**: ቴክኒካዊ ቁጥጥሮች ከደህንነት ግንዛቤ ጋር መጣመር አለባቸው
- **የአደጋ ዝርግርግ**: አዳዲስ የጥቃት ዘዴዎች አሁኑን ጥበቃ ማለፍ ይችላሉ

## 🎯 የምሳሌ ጥቃት ሁኔታዎች

Ghost የተለመዱ የጥቃት ቬክተሮችን ቢያነጣጥርም፣ ልዩ መከላከያ በተገቢው አተገባበር እና ፈተና ላይ ይመረኮዛል:

### WannaCry-አይነት ጥቃቶች
- **ቅነሳ**: `Set-Ghost -SMBv1` ደካማውን ፕሮቶኮል ያሰናክላል
- **ግምት**: ምንም legacy ስርዓቶች SMBv1 እንደማይፈልጉ ያረጋግጡ

### በRDP ላይ የተመሰረቱ Ransomware
- **ቅነሳ**: `Set-Ghost -RDP` remote desktop መዳረሻን ይዘጋል
- **ግምት**: አማራጭ የርቀት መዳረሻ ዘዴዎችን ሊፈልግ ይችላል

### በሰነድ ላይ የተመሰረተ Malware
- **ቅነሳ**: `Set-Ghost -Macros` የማክሮ አፈጻጸምን ያሰናክላል
- **ግምት**: ህጋዊ በማክሮ የነቁ ሰነዶችን ሊጎዳ ይችላል

### በUSB የሚደርሱ ስጋቶች
- **ቅነሳ**: `Set-Ghost -USBStorage -AutoRun` የUSB ተግባርን ይገድባል
- **ግምት**: ህጋዊ የUSB መሳሪያ አጠቃቀምን ሊጎዳ ይችላል

## 🏢 የድርጅት ባህሪያት

### Group Policy ድጋፍ
```powershell
# ቅንብሮችን በGroup Policy ሪጅስትሪ በኩል ይተግብሩ
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# ከGP ማደስ በኋላ ቅንብሮች በዶሜይን ላይ ይተገበራሉ
gpupdate /force
```

### Microsoft Intune ውህደት
```powershell
# ለGhost ቅንብሮች Intune ፖሊሲዎችን ይፍጠሩ
Set-IntuneGhost -Settings $GhostSettings -Interactive

# ፖሊሲዎች በራስ ሰር ወደ የሚተዳደሩ መሳሪያዎች ይሰማራሉ
```

### የመቀጠል ሪፖርት
```powershell
# የደህንነት ግምገማ ሪፖርት ይፍጠሩ
Get-Ghost | Export-Csv -Path "SecurityAudit-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Azure የደህንነት አቋም ሪፖርት
Get-AzureGhost | Out-File "AzureSecurityReport.txt"
```

## 📚 የተሻሉ ልምዶች

### ቅድመ-ማሰማራት
1. **የአሁኑን ሁኔታ ዘግብ**: ከለውጦች በፊት `Get-Ghost` ን ያሄዱ
2. **በጥልቀት ይፈትኑ**: በምርት-ያልሆነ አካባቢ ውስጥ ያረጋግጡ
3. **መመለሻ እቅድ**: እያንዳንዱን ቅንብር እንዴት መመለስ እንደሚችሉ ያውቁ
4. **የባለድርሻ አካላት ግምገማ**: የንግድ ክፍሎች ለውጦችን እንደሚያጸድቁ ያረጋግጡ

### በማሰማራት ጊዜ
1. **ደረጃ በደረጃ አቀራረብ**: መጀመሪያ ወደ ፓይለት ቡድኖች ይሰማሩ
2. **ተጽእኖን ይቆጣጠሩ**: የተጠቃሚ ቅሬታዎችን ወይም የስርዓት ችግሮችን ይመልከቱ
3. **ችግሮችን ዘግብ**: ለወደፊት ማጣቀሻ ማንኛውንም ችግር ይመዝግቡ
4. **ለውጦችን ያሳውቁ**: ተጠቃሚዎችን ስለ ደህንነት ማሻሻያዎች ያሳውቁ

### ከማሰማራት በኋላ
1. **መደበኛ ግምገማ**: ቅንብሮችን ለማረጋገጥ በጊዜ ገደብ `Get-Ghost` ን ያሄዱ
2. **ሰነድ አዘምን**: የደህንነት ውቅሮችን ወቅታዊ ያድርጉ
3. **ውጤታማነትን ይገምግሙ**: ለደህንነት ሁኔታዎች ይቆጣጠሩ
4. **ቀጣይ ማሻሻያ**: በአደጋ መልክዓ ምድር ላይ በመመርኮዝ ቅንብሮችን ያስተካክሉ

## 🔧 ችግር መፍታት

### የተለመዱ ችግሮች
- **የፈቃድ ስህተቶች**: የተነሳ PowerShell ክፍለ ጊዜ ያረጋግጡ
- **የአገልግሎት ጥገኝነቶች**: አንዳንድ አገልግሎቶች ጥገኝነቶች ሊኖራቸው ይችላል
- **የመተግበሪያ ተኳኋኝነት**: ከንግድ መተግበሪያዎች ጋር ይፈትኑ
- **የአውታረ መረብ ግንኙነት**: የርቀት መዳረሻ አሁንም እንደሚሰራ ያረጋግጡ

### የማገገሚያ አማራጮች
```powershell
# ሲፈልጉ ልዩ አገልግሎቶችን እንደገና ያንቁ
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 ስለ ደራሲው

**Jim Tyler** - ለPowerShell Microsoft MVP
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ ተመዝግበዋል)
- **ጋዜጣ**: [PowerShell.News](https://powershell.news) - ሳሳናዊ የደህንነት መረጃ
- **ደራሲ**: "PowerShell for Systems Engineers"
- **ልምድ**: የPowerShell ራስ-ሰር መሳሪያ እና Windows ደህንነት አሊያዎች

## 📄 ፍቃድ እና መከልከያ

### MIT ፍቃድ
Ghost በMIT ፍቃድ ስር ለነጻ አጠቃቀም፣ ለመቀየር እና ለማሰራጨት ይቀርባል።

### የደህንነት መከልከያ
- **ምንም ዋስትና የለም**: Ghost "እንደዚ ፈጠረኛ" ያለ ምንም አይነት ዋስትና ይሰጣል
- **ፈተና ያስፈልጋል**: ሁሌም በምርት-ያልሆኑ አካባቢዎች ውስጥ መጀመሪያ ይፈትኑ
- **ሙያዊ መመሪያ**: ለምርት ማሰማራቶች ከደህንነት ባለሙያዎች ጋር ይማከሩ
- **የአሠራር ተጽእኖ**: ደራሲዎች ለማንኛውም የአሠራር ማቋረጥ ተጠያቂ አይደሉም
- **አጠቃላይ ደህንነት**: Ghost የሙሉ የደህንነት ስትራቴጂ አንድ አካል ነው

### ድጋፍ
- **GitHub ችግሮች**: [ሳንካዎችን ሪፖርት ያድርጉ ወይም ባህሪያትን ይጠይቁ](https://github.com/jimrtyler/Ghost/issues)
- **ሰነድ**: ለዝርዝር እርዳታ `Get-Help <function> -Full` ይጠቀሙ
- **ማህበረሰብ**: PowerShell እና ደህንነት ማህበረሰብ መድረኮች

---

**🔐 ከGhost ጋር የእርስዎን የደህንነት አቋም ያጠናክሩ - ግን ሁሌም መጀመሪያ ይፈትኑ።**

```powershell
# በግምት ሳይሆን በግምገማ ይጀምሩ
Get-Ghost
```

**⭐ Ghost የእርስዎን የደህንነት አቋም ለማሻሻል ከረዳ ይህንን repository ይዩትን!**