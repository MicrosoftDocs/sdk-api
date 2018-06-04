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

# tagDEVNAMES structure


## -description


Contains strings that identify the driver, device, and output port names for a printer. These strings must be ANSI strings when the ANSI version of <a href="https://msdn.microsoft.com/c8dd658e-04a2-489f-99cc-50810feb3df7">PrintDlg</a> or <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> is used, and must be Unicode strings when the Unicode version of <b>PrintDlg</b> or <b>PrintDlgEx</b> is used. The <b>PrintDlgEx</b> and <b>PrintDlg</b> functions use these strings to initialize the system-defined <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a> or <a href="https://msdn.microsoft.com/34f69b25-8a89-4322-af4c-a80b85a4a973">Print Dialog Box</a>. When the user closes the property sheet or dialog box, information about the selected printer is returned in this structure. 


## -struct-fields




### -field wDriverOffset

Type: <b>WORD</b>

The offset, in characters, from the beginning of this structure to a null-terminated string that contains the file name (without the extension) of the device driver. On input, this string is used to determine the printer to display initially in the dialog box. 


### -field wDeviceOffset

Type: <b>WORD</b>

The offset, in characters, from the beginning of this structure to the null-terminated string that contains the name of the device. 


### -field wOutputOffset

Type: <b>WORD</b>

The offset, in characters, from the beginning of this structure to the null-terminated string that contains the device name for the physical output medium (output port). 


### -field wDefault

Type: <b>WORD</b>

Indicates whether the strings contained in the <b>DEVNAMES</b> structure identify the default printer. This string is used to verify that the default printer has not changed since the last print operation. If any of the strings do not match, a warning message is displayed informing the user that the document may need to be reformatted. On output, the <b>wDefault</b> member is changed only if the <b>Print Setup</b> dialog box was displayed and the user chose the <b>OK</b> button. The <b>DN_DEFAULTPRN</b> flag is used if the default printer was selected. If a specific printer is selected, the flag is not used. All other flags in this member are reserved for internal use by the dialog box procedure for the <b>Print</b> property sheet or <b>Print</b> dialog box. 


## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/c8dd658e-04a2-489f-99cc-50810feb3df7">PrintDlg</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>
 

 

