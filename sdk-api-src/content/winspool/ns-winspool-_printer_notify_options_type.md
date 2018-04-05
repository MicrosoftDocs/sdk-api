---
UID: NS:winspool._PRINTER_NOTIFY_OPTIONS_TYPE
title: "_PRINTER_NOTIFY_OPTIONS_TYPE"
author: windows-driver-content
description: The PRINTER_NOTIFY_OPTIONS_TYPE structure specifies the set of printer or job information fields to be monitored by a printer change notification object.A call to the FindFirstPrinterChangeNotification function specifies a PRINTER_NOTIFY_OPTIONS structure, which contains an array of PRINTER_NOTIFY_OPTIONS_TYPE structures.
old-location: gdi\printer_notify_options_type.htm
old-project: printdocs
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE, JOB_NOTIFY_TYPE, PPRINTER_NOTIFY_OPTIONS_TYPE, PPRINTER_NOTIFY_OPTIONS_TYPE structure pointer [Windows GDI], PRINTER_NOTIFY_OPTIONS_TYPE, PRINTER_NOTIFY_OPTIONS_TYPE structure [Windows GDI], PRINTER_NOTIFY_TYPE, _PRINTER_NOTIFY_OPTIONS_TYPE, _win32_PRINTER_NOTIFY_OPTIONS_TYPE_str, gdi.printer_notify_options_type, winspool/PPRINTER_NOTIFY_OPTIONS_TYPE, winspool/PRINTER_NOTIFY_OPTIONS_TYPE"
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE, *LPPRINTER_NOTIFY_OPTIONS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINTER_NOTIFY_OPTIONS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PRINTER_NOTIFY_OPTIONS_TYPE structure


## -description



The <b>PRINTER_NOTIFY_OPTIONS_TYPE</b> structure specifies the set of printer or job information fields to be monitored by a printer change notification object.

A call to the 
              <a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a> function specifies a 
              <a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a> structure, which contains an array of 
         <b>PRINTER_NOTIFY_OPTIONS_TYPE</b>  structures.




## -struct-fields




### -field Type

The type to be watched. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="JOB_NOTIFY_TYPE"></a><a id="job_notify_type"></a><dl>
<dt><b>JOB_NOTIFY_TYPE</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Indicates that the fields specified in the <b>pFields</b> array are JOB_NOTIFY_FIELD_* constants.

</td>
</tr>
<tr>
<td width="40%"><a id="PRINTER_NOTIFY_TYPE"></a><a id="printer_notify_type"></a><dl>
<dt><b>PRINTER_NOTIFY_TYPE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Indicates that the fields specified in the <b>pFields</b> array are PRINTER_NOTIFY_FIELD_* constants.

</td>
</tr>
</table>
 


### -field Reserved0

Reserved.


### -field Reserved1

Reserved.


### -field Reserved2

Reserved.


### -field Count

The number of elements in the <b>pFields</b> array.


### -field pFields

A pointer to an array of values. Each element of the array specifies a job or printer information field of interest. For a list of supported printer and job information fields, see the <a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548837">FindFirstPrinterChangeNotification</a>



<a href="https://msdn.microsoft.com/7a7b9e01-32e0-47f8-a5b1-5f7e6a663714">PRINTER_NOTIFY_INFO_DATA</a>



<a href="https://msdn.microsoft.com/712c546d-dbb3-4f78-b14e-fbb8619b57f9">PRINTER_NOTIFY_OPTIONS</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

