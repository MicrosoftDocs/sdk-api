---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

