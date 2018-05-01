---
UID: NF:wiautil.WIAS_LERROR
title: WIAS_LERROR macro
author: windows-driver-content
description: The WIAS_LERROR macro is obsolete for Windows Vista and later. It is recommended that the WIAS_ERROR macro be used instead.The WIAS_LERROR macro writes a diagnostic WIA_ERROR message to the log file.
old-location: image\wias_lerror.htm
old-project: image
ms.assetid: 71949653-08c7-4f22-951d-6e1595b10700
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_b765e146-4e57-447c-9e9d-0f3cdc784291.xml, WIAS_LERROR, WIAS_LERROR macro [Imaging Devices], image.wias_lerror, wiamdef/WIAS_LERROR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me, Windows XP, and later. Obsolete for Windows Vista and later. Use WIAS_ERROR instead.
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
-	WIAS_LERROR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_LERROR macro


## -description


The WIAS_LERROR macro is obsolete for Windows Vista and later. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549565">WIAS_ERROR</a> macro be used instead.

The WIAS_LERROR macro writes a diagnostic WIA_ERROR message to the log file.


## -parameters




### -param x

TBD


### -param y

TBD


### -param params

TBD






####### - format_string, ...

Specifies a variable argument list, which starts with an ANSI format string that describes the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".


#### - lResId

Specifies the resource ID. This value should be set to WIALOG_NO_RESOURCE_ID.


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
<pre>WIAS_LERROR(g_pIWiaLog, WIALOG_NO_RESOURCE_ID,
("MyClass::MyMethod, This is my text and my lValue = %d", lValue));</pre>
</td>
</tr>
</table></span></div>
The WIAS_LERROR macro is not recommended for Windows Vista, because it does not record its output to the <i>Wiatrace.log </i>diagnostic log file. It is recommended that the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549565">WIAS_ERROR</a> macro be used instead. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549565">WIAS_ERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549589">WIAS_LHRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549600">WIAS_LTRACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549610">WIAS_LWARNING</a>
 

 

