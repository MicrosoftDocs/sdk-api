---
UID: NE:shldisp.ShellSpecialFolderConstants
title: ShellSpecialFolderConstants
author: windows-sdk-content
description: Specifies unique, system-independent values that identify special folders.
old-location: shell\ShellSpecialFolderConstants.htm
tech.root: shell
ms.assetid: 35338102-f3a9-4bcf-ad62-d395462e6d2c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ShellSpecialFolderConstants, ShellSpecialFolderConstants enumeration [Windows Shell], _win32_ShellSpecialFolderConstants, shell.ShellSpecialFolderConstants, shldisp/ShellSpecialFolderConstants, shldisp/ssfALTSTARTUP, shldisp/ssfAPPDATA, shldisp/ssfBITBUCKET, shldisp/ssfCOMMONALTSTARTUP, shldisp/ssfCOMMONAPPDATA, shldisp/ssfCOMMONDESKTOPDIR, shldisp/ssfCOMMONFAVORITES, shldisp/ssfCOMMONPROGRAMS, shldisp/ssfCOMMONSTARTMENU, shldisp/ssfCOMMONSTARTUP, shldisp/ssfCONTROLS, shldisp/ssfCOOKIES, shldisp/ssfDESKTOP, shldisp/ssfDESKTOPDIRECTORY, shldisp/ssfDRIVES, shldisp/ssfFAVORITES, shldisp/ssfFONTS, shldisp/ssfHISTORY, shldisp/ssfINTERNETCACHE, shldisp/ssfLOCALAPPDATA, shldisp/ssfMYPICTURES, shldisp/ssfNETHOOD, shldisp/ssfNETWORK, shldisp/ssfPERSONAL, shldisp/ssfPRINTERS, shldisp/ssfPRINTHOOD, shldisp/ssfPROFILE, shldisp/ssfPROGRAMFILES, shldisp/ssfPROGRAMFILESx86, shldisp/ssfPROGRAMS, shldisp/ssfRECENT, shldisp/ssfSENDTO, shldisp/ssfSTARTMENU, shldisp/ssfSTARTUP, shldisp/ssfSYSTEM, shldisp/ssfSYSTEMx86, shldisp/ssfTEMPLATES, shldisp/ssfWINDOWS, ssfALTSTARTUP, ssfAPPDATA, ssfBITBUCKET, ssfCOMMONALTSTARTUP, ssfCOMMONAPPDATA, ssfCOMMONDESKTOPDIR, ssfCOMMONFAVORITES, ssfCOMMONPROGRAMS, ssfCOMMONSTARTMENU, ssfCOMMONSTARTUP, ssfCONTROLS, ssfCOOKIES, ssfDESKTOP, ssfDESKTOPDIRECTORY, ssfDRIVES, ssfFAVORITES, ssfFONTS, ssfHISTORY, ssfINTERNETCACHE, ssfLOCALAPPDATA, ssfMYPICTURES, ssfNETHOOD, ssfNETWORK, ssfPERSONAL, ssfPRINTERS, ssfPRINTHOOD, ssfPROFILE, ssfPROGRAMFILES, ssfPROGRAMFILESx86, ssfPROGRAMS, ssfRECENT, ssfSENDTO, ssfSTARTMENU, ssfSTARTUP, ssfSYSTEM, ssfSYSTEMx86, ssfTEMPLATES, ssfWINDOWS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shldisp.h
api_name:
 - ShellSpecialFolderConstants
product: Windows
targetos: Windows
req.typenames: ShellSpecialFolderConstants
req.redist: 
---

# ShellSpecialFolderConstants enumeration


## -description


Specifies unique, system-independent values that identify special folders. These folders are frequently used by applications but which may not have the same name or location on any given system. For example, the system folder can be "C:\Windows" on one system and "C:\Winnt" on another.


## -enum-fields




### -field ssfDESKTOP

0x00 (0). Windows desktop—the virtual folder that is the root of the namespace.


### -field ssfPROGRAMS

0x02 (2). File system directory that contains the user's program groups (which are also file system directories). A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs.


### -field ssfCONTROLS

0x03 (3). Virtual folder that contains icons for the Control Panel applications.


### -field ssfPRINTERS

0x04 (4). Virtual folder that contains installed printers.


### -field ssfPERSONAL

0x05 (5). File system directory that serves as a common repository for a user's documents. A typical path is C:\Users\<i>username</i>\Documents.


### -field ssfFAVORITES

0x06 (6). File system directory that serves as a common repository for the user's favorite URLs. A typical path is C:\Documents and Settings\<i>username</i>\Favorites.


### -field ssfSTARTUP

0x07 (7). File system directory that corresponds to the user's Startup program group. The system starts these programs whenever any user first logs into their profile after a reboot. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\StartUp.


### -field ssfRECENT

0x08 (8). File system directory that contains the user's most recently used documents. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Recent.


### -field ssfSENDTO

0x09 (9). File system directory that contains <b>Send To</b> menu items. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\SendTo.


### -field ssfBITBUCKET

0x0a (10). Virtual folder that contains the objects in the user's Recycle Bin.


### -field ssfSTARTMENU

0x0b (11). File system directory that contains <b>Start</b> menu items. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Start Menu.


### -field ssfDESKTOPDIRECTORY

0x10 (16). File system directory used to physically store the file objects that are displayed on the desktop. It is not to be confused with the desktop folder itself, which is a virtual folder. A typical path is C:\Documents and Settings\<i>username</i>\Desktop.


### -field ssfDRIVES

0x11 (17). My Computer—the virtual folder that contains everything on the local computer: storage devices, printers, and Control Panel. This folder can also contain mapped network drives.


### -field ssfNETWORK

0x12 (18). Network Neighborhood—the virtual folder that represents the root of the network namespace hierarchy.


### -field ssfNETHOOD

0x13 (19). A file system folder that contains any link objects in the <b>My Network Places</b> virtual folder. It is not the same as ssfNETWORK, which represents the network namespace root. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Network Shortcuts.


### -field ssfFONTS

0x14 (20). Virtual folder that contains installed fonts. A typical path is C:\Windows\Fonts.


### -field ssfTEMPLATES

0x15 (21). File system directory that serves as a common repository for document templates.


### -field ssfCOMMONSTARTMENU

0x16 (22). File system directory that contains the programs and folders that appear on the <b>Start</b> menu for all users. A typical path is C:\Documents and Settings\All Users\Start Menu. Valid only for Windows NT systems.


### -field ssfCOMMONPROGRAMS

0x17 (23). File system directory that contains the directories for the common program groups that appear on the <b>Start</b> menu for all users. A typical path is C:\Documents and Settings\All Users\Start Menu\Programs. Valid only for Windows NT systems.


### -field ssfCOMMONSTARTUP

0x18 (24). File system directory that contains the programs that appear in the Startup folder for all users. A typical path is C:\Documents and Settings\All Users\Microsoft\Windows\Start Menu\Programs\StartUp. Valid only for Windows NT systems.


### -field ssfCOMMONDESKTOPDIR

0x19 (25). File system directory that contains files and folders that appear on the desktop for all users. A typical path is C:\Documents and Settings\All Users\Desktop. Valid only for Windows NT systems.


### -field ssfAPPDATA

0x1a (26). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 4.71</a>. File system directory that serves as a common repository for application-specific data. A typical path is C:\Documents and Settings\<i>username</i>\Application Data.


### -field ssfPRINTHOOD

0x1b (27). File system directory that contains any link objects in the Printers virtual folder. A typical path is C:\Users\<i>username</i>\AppData\Roaming\Microsoft\Windows\Printer Shortcuts.


### -field ssfLOCALAPPDATA

0x1c (28). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. File system directory that serves as a data repository for local (non-roaming) applications. A typical path is C:\Users\<i>username</i>\AppData\Local.


### -field ssfALTSTARTUP

0x1d (29). File system directory that corresponds to the user's non-localized Startup program group.


### -field ssfCOMMONALTSTARTUP

0x1e (30). File system directory that corresponds to the non-localized Startup program group for all users. Valid only for Windows NT systems.


### -field ssfCOMMONFAVORITES

0x1f (31). File system directory that serves as a common repository for the favorite URLs shared by all users. Valid only for Windows NT systems.


### -field ssfINTERNETCACHE

0x20 (32). File system directory that serves as a common repository for temporary Internet files. A typical path is C:\Users\<i>username</i>\AppData\Local\Microsoft\Windows\Temporary Internet Files.


### -field ssfCOOKIES

0x21 (33). File system directory that serves as a common repository for Internet cookies. A typical path is C:\Documents and Settings\<i>username</i>\Application Data\Microsoft\Windows\Cookies.


### -field ssfHISTORY

0x22 (34). File system directory that serves as a common repository for Internet history items.


### -field ssfCOMMONAPPDATA

0x23 (35). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Application data for all users. A typical path is C:\Documents and Settings\All Users\Application Data.


### -field ssfWINDOWS

0x24 (36). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Windows directory. This corresponds to the %windir% or %SystemRoot% environment variables. A typical path is C:\Windows.


### -field ssfSYSTEM

0x25 (37). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. The System folder. A typical path is C:\Windows\System32.


### -field ssfPROGRAMFILES

0x26 (38). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. Program Files folder. A typical path is C:\Program Files.


### -field ssfMYPICTURES

0x27 (39). My Pictures folder. A typical path is C:\Users\<i>username</i>\Pictures.


### -field ssfPROFILE

0x28 (40). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. User's profile folder.


### -field ssfSYSTEMx86

0x29 (41). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. System folder. A typical path is C:\Windows\System32, or C:\Windows\Syswow32 on a 64-bit computer.


### -field ssfPROGRAMFILESx86

0x30 (48). <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 6.0</a>. Program Files folder. A typical path is C:\Program Files, or C:\Program Files (X86) on a 64-bit computer.


## -remarks



The values in this enumeration are equivalent to their corresponding <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> or <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values, used in C++ applications. They supersede the use of environment variables for this purpose. Note that not all <b>CSIDL</b> or <b>KNOWNFOLDERID</b> values have an equivalent value in <b>ShellSpecialFolderConstants</b>.

<div class="alert"><b>Note</b>   Where a constant identifies a file system folder, a commonly used path on Windows Vista systems is given as an example. However, there is no guarantee that this path will be used on any particular system, including Windows Vista systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a>



<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>
 

 

