---
UID: NS:tapi.lineappinfo_tag
title: lineappinfo_tag
author: windows-sdk-content
description: The LINEAPPINFO structure contains information about the application that is currently running. The LINEDEVSTATUS structure can contain an array of LINEAPPINFO structures.
old-location: tapi2\lineappinfo_str.htm
old-project: Tapi
ms.assetid: 1c1d2d31-a234-407e-b9fc-4823928c5ca1
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*LPLINEAPPINFO, LINEAPPINFO, LINEAPPINFO structure [TAPI 2.2], LPLINEAPPINFO, LPLINEAPPINFO structure pointer [TAPI 2.2], _tapi2_lineappinfo_str, lineappinfo_tag, tapi/LINEAPPINFO, tapi/LPLINEAPPINFO, tapi2.lineappinfo_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: LINEAPPINFO, *LPLINEAPPINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEAPPINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineappinfo_tag structure


## -description


The 
<b>LINEAPPINFO</b> structure contains information about the application that is currently running. The 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> structure can contain an array of 
<b>LINEAPPINFO</b> structures.


## -struct-fields




### -field dwMachineNameSize

Size of the computer name string including the <b>null</b> terminator, in bytes.


### -field dwMachineNameOffset

Offset from the beginning of the 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> structure to a string specifying the name of the computer on which the application is executing. The size of the field is specified by <b>dwMachineNameSize</b>.


### -field dwUserNameSize

Size of the user name string including the <b>null</b> terminator, in bytes.


### -field dwUserNameOffset

Offset from the beginning of the 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> structure to a string specifying the user name under whose account the application is running. The size of the field is specified by <b>dwUserNameSize</b>.


### -field dwModuleFilenameSize

Size of the module file name string, in bytes.


### -field dwModuleFilenameOffset

Offset from the beginning of 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> to a string specifying the module file name of the application. This string can be used in a call to 
<a href="https://msdn.microsoft.com/931c2fa4-dad6-432d-8f07-bb04b646916b">lineHandoff</a> to perform a directed handoff to the application. The size of the field is specified by <b>dwModuleFilenameSize</b>.


### -field dwFriendlyNameSize

Size of the display name string, in bytes.


### -field dwFriendlyNameOffset

Offset from the beginning of 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> to the string provided by the application to 
<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a> or 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>, which should be used in any display to the user. The size of the field is specified by <b>dwFriendlyNameSize</b>.


### -field dwMediaModes

Media types for which the application has requested ownership of new calls; zero if when it opened the line <b>dwPrivileges</b> did not include LINECALLPRIVILEGE_OWNER.


### -field dwAddressID

If the line handle was opened using LINEOPENOPTION_SINGLEADDRESS, contains the address identifier specified; set to 0xFFFFFFFF if the single address option was not used. 




An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


## -see-also




<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>



<a href="https://msdn.microsoft.com/14f7944b-e967-4967-9fb2-e7aeb78bb045">TSPI_lineGetLineDevStatus</a>



<a href="https://msdn.microsoft.com/9c0fa2ba-1157-43d2-af56-aa4e0c28bd05">lineGetLineDevStatus</a>



<a href="https://msdn.microsoft.com/931c2fa4-dad6-432d-8f07-bb04b646916b">lineHandoff</a>



<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

