---
UID: NF:wiautil.WIAS_LWARNING
title: WIAS_LWARNING macro
author: windows-driver-content
description: The WIAS_LWARNING macro is obsolete for Windows Vista and later.The WIAS_LWARNING macro writes a diagnostic WIA_WARNING message to the log file.
old-location: image\wias_lwarning.htm
old-project: image
ms.assetid: 2959c470-1da7-4396-a591-7a356379f9de
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_bac21803-be4c-4ce0-a241-b9380cb627ab.xml, WIAS_LWARNING, WIAS_LWARNING macro [Imaging Devices], image.wias_lwarning, wiamdef/WIAS_LWARNING
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me, Windows XP, and later. Obsolete for Windows Vista and later.
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
-	WIAS_LWARNING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_LWARNING macro


## -description


The WIAS_LWARNING macro is obsolete for Windows Vista and later.

The WIAS_LWARNING macro writes a diagnostic WIA_WARNING message to the log file.


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
<pre>WIAS_LWARNING(g_pIWiaLog, WIALOG_NO_RESOURCE_ID,
  ("MyClass::MyMethod, This is my text and my lValue = %d", lValue));</pre>
</td>
</tr>
</table></span></div>
Please note that it does not write to the new log file used in Windows Vista and later.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549580">WIAS_LERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549589">WIAS_LHRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549600">WIAS_LTRACE</a>
 

 

