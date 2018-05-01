---
UID: NF:wiautil.WIAS_LTRACE
title: WIAS_LTRACE macro
author: windows-driver-content
description: The WIAS_LTRACE macro is obsolete for Windows Vista and later. It is recommended that the WIAS_TRACE macro be used instead.The WIAS_LTRACE macro writes a diagnostic WIA_TRACE message to the log file.
old-location: image\wias_ltrace.htm
old-project: image
ms.assetid: 513fd718-3d35-4a7b-be28-b002a8108e86
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_bb7ae826-5b43-47c1-bf94-bd491d8b91a7.xml, WIAS_LTRACE, WIAS_LTRACE macro [Imaging Devices], image.wias_ltrace, wiamdef/WIAS_LTRACE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me, Windows XP, and later versions of the operating system. Obsolete for Windows Vista and later. Use WIAS_TRACE instead.
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
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamdef.h
api_name:
-	WIAS_LTRACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_LTRACE macro


## -description


The WIAS_LTRACE macro is obsolete for Windows Vista and later. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549619">WIAS_TRACE</a> macro be used instead.

The WIAS_LTRACE macro writes a diagnostic WIA_TRACE message to the log file.


## -parameters




### -param x

TBD


### -param y

TBD


### -param z

TBD


### -param params

TBD






#### - DetailLevel

Specifies the diagnostic detail level of the message. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
WIALOG_LEVEL1

</td>
<td>
Logs entry and exit points for all WIA methods and functions.

</td>
</tr>
<tr>
<td>
WIALOG_LEVEL2

</td>
<td>
Logs additional details for WIALOG_LEVEL1.

</td>
</tr>
<tr>
<td>
WIALOG_LEVEL3

</td>
<td>
Logs entry and exit points for all WIA methods and functions and additional vendor-supplied functions.

</td>
</tr>
<tr>
<td>
WIALOG_LEVEL4

</td>
<td>
Logs additional details for WIALOG_LEVEL3. 

</td>
</tr>
<tr>
<td>
WIALOG_LEVELXXX

</td>
<td>
User-defined log levels.

</td>
</tr>
</table>
 


#### - ResourceID

Specifies the resource ID. This value should be set to WIALOG_NO_RESOURCE_ID.


#### - format_string

Specifies a variable argument list, which starts with an ANSI format string describing the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".


#### - pIWiaLog

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff543935">IWiaLog Interface</a>.


## -remarks



The following is an example of how the macro can be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WIAS_LTRACE(g_pIWiaLog, WIALOG_NO_RESOURCE_ID, WIALOG_LEVEL2,
  ("MyClass::MyMethod, This is my text and my lValue = %d", lValue));</pre>
</td>
</tr>
</table></span></div>
The WIAS_LTRACE macro is not recommended for Windows Vista, because it does not record its output to the <i>Wiatrace.log </i>diagnostic Log file. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549619">WIAS_TRACE</a> macro be used instead. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549580">WIAS_LERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549589">WIAS_LHRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549610">WIAS_LWARNING</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549619">WIAS_TRACE</a>
 

 

