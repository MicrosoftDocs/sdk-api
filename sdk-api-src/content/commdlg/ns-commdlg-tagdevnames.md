---
UID: NS:commdlg.tagDEVNAMES
title: tagDEVNAMES
author: windows-sdk-content
description: Contains strings that identify the driver, device, and output port names for a printer.
old-location: dlgbox\devnames_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\devnames.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*LPDEVNAMES, DEVNAMES, DEVNAMES structure [Dialog Boxes], LPDEVNAMES, LPDEVNAMES structure pointer [Dialog Boxes], _win32_DEVNAMES_str, _win32_devnames_str_cpp, commdlg/DEVNAMES, commdlg/LPDEVNAMES, dlgbox.devnames_str, tagDEVNAMES, winui._win32_devnames_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Commdlg.h
api_name:
 - DEVNAMES
product: Windows
targetos: Windows
req.typenames: DEVNAMES
req.redist: 
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
 

 

