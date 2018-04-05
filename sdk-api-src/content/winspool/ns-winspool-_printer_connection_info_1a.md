---
UID: NS:winspool._PRINTER_CONNECTION_INFO_1A
title: "_PRINTER_CONNECTION_INFO_1A"
author: windows-driver-content
description: Represents information about a connection to a printer.
old-location: gdi\printer_connection_info_1.htm
old-project: printdocs
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PPRINTER_CONNECTION_INFO_1A, PPRINTER_CONNECTION_INFO_1, PPRINTER_CONNECTION_INFO_1 structure pointer [Windows GDI], PRINTER_CONNECTION_INFO_1, PRINTER_CONNECTION_INFO_1 structure [Windows GDI], PRINTER_CONNECTION_INFO_1A, _PRINTER_CONNECTION_INFO_1A, _PRINTER_CONNECTION_INFO_1W, _win32_PRINTER_CONNECTION_INFO_1_str, gdi.printer_connection_info_1, winspool/PPRINTER_CONNECTION_INFO_1, winspool/PRINTER_CONNECTION_INFO_1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_CONNECTION_INFO_1A, *PPRINTER_CONNECTION_INFO_1A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_CONNECTION_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_CONNECTION_INFO_1A structure


## -description



Represents information about a connection to a printer.




## -struct-fields




### -field dwFlags

The following values are defined:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_CONNECTION_MISMATCH (0x00000020)</td>
<td>
If this bit-flag is set, the printer connection is mismatched. The user can supply a local print driver as <i>pszDriverName</i> and use it to do the rendering instead of using the driver installed on the server printer to which the user is connected.

</td>
</tr>
<tr>
<td>PRINTER_CONNECTION_NO_UI (0x00000040)</td>
<td>
If this bit-flag is set then this call cannot display a dialog box. If a dialog box must be displayed to install a printer driver from the server and this bit-flag is set, the printer driver will not be installed, the printer connection will not be added, and the call will fail.

<b>Windows 7:</b> In Windows 7 and later versions of Windows, if this flag is set and the user is running in elevated mode, the <b>Do you trust this printer?</b> dialog will not be shown.

</td>
</tr>
</table>
 


### -field pszDriverName

A pointer to the name of the driver.


## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

