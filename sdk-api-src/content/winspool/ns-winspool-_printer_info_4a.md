---
UID: NS:winspool._PRINTER_INFO_4A
title: "_PRINTER_INFO_4A"
author: windows-driver-content
description: The PRINTER_INFO_4 structure specifies general printer information.The structure can be used to retrieve minimal printer information on a call to EnumPrinters.
old-location: gdi\printer_info_4.htm
old-project: printdocs
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_INFO_4A, *PPRINTER_INFO_4A, PPRINTER_INFO_4, PPRINTER_INFO_4 structure pointer [Windows GDI], PRINTER_INFO_4, PRINTER_INFO_4 structure [Windows GDI], PRINTER_INFO_4A, _PRINTER_INFO_4A, _PRINTER_INFO_4W, _win32_PRINTER_INFO_4_str, gdi.printer_info_4, winspool/PPRINTER_INFO_4, winspool/PRINTER_INFO_4, winspool/_PRINTER_INFO_4A, winspool/_PRINTER_INFO_4W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_PRINTER_INFO_4W (Unicode) and _PRINTER_INFO_4A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_INFO_4A, *PPRINTER_INFO_4A, *LPPRINTER_INFO_4A
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_INFO_4
-	_PRINTER_INFO_4A
-	_PRINTER_INFO_4W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_INFO_4A structure


## -description



The <b>PRINTER_INFO_4</b> structure specifies general printer information.

The structure can be used to retrieve minimal printer information on a call to 
        <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>. Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.




## -struct-fields




### -field pPrinterName

Pointer to a null-terminated string that specifies the name of the printer (local or remote).


### -field pServerName

Pointer to a null-terminated string that is the name of the server.


### -field Attributes

Specifies information about the returned data.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_LOCAL</td>
<td>The printer is a local printer.</td>
</tr>
<tr>
<td>PRINTER_ATTRIBUTE_NETWORK</td>
<td>The printer is a remote printer.</td>
</tr>
</table>
 


## -remarks



The <b>PRINTER_INFO_4</b> structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established. When <a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a> is called with a <b>PRINTER_INFO_4</b> data structure, that function queries the registry for the specified information, then returns immediately. This differs from the behavior of <b>EnumPrinters</b> when called with other levels of <b>PRINTER_INFO_xxx</b> data structures. In particular, when <b>EnumPrinters</b> is called with a level 2 (<b>PRINTER_INFO_2</b>  ) data structure, it performs an <b>OpenPrinter</b> call on each remote connection. If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the <b>OpenPrinter</b> call. This can take a while. Passing a <b>PRINTER_INFO_4</b> structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent <b>EnumPrinter</b> level 2 call can be made.
		

<b>Attributes</b> can also contain values that are defined in the <b>Attributes</b> field of <b>PRINTER_INFO_2</b>.

Some printer configurations, such as printer connections to some non-Windows-based print servers,  might return both <b>PRINTER_ATTRIBUTE_LOCAL</b> and <b>PRINTER_ATTRIBUTE_NETWORK</b>.




## -see-also




<a href="https://msdn.microsoft.com/0d0cc726-c515-4146-9273-cdf1db3c76b7">EnumPrinters</a>



<a href="https://msdn.microsoft.com/f162edbb-83ee-40c3-8710-9c867301d652">GetPrinter</a>



<a href="https://msdn.microsoft.com/96763220-d851-46f0-8be8-403f3356edb9">OpenPrinter</a>



<a href="https://msdn.microsoft.com/0b0e2d0e-2625-4cab-a8f9-536185479443">PRINTER_INFO_1</a>



<a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>



<a href="https://msdn.microsoft.com/527d635d-2d75-4b56-bab7-e95c9919a8fb">PRINTER_INFO_3</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

