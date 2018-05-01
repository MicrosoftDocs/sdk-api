---
UID: NF:wiamdef.WIAS_TRACE
title: WIAS_TRACE macro
author: windows-driver-content
description: The WIAS_TRACE macro writes a diagnostic message to the Wiatrace.log file.
old-location: image\wias_trace.htm
old-project: image
ms.assetid: 9f6b06bf-60d3-4ec2-8c49-405bff2ccb5e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_c755ea6c-c312-4b15-be83-a437358b83a9.xml, WIAS_TRACE, WIAS_TRACE macro [Imaging Devices], image.wias_trace, wiamdef/WIAS_TRACE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiamdef.h
req.include-header: Wiautil.h
req.target-type: Desktop
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
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamdef.h
api_name:
-	WIAS_TRACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_TRACE macro


## -description


The WIAS_TRACE macro writes a diagnostic message to the <i>Wiatrace.log</i> file.


## -parameters




### -param x

TBD






#### - HInst

Handle to the DLL (driver).


####### - format_string, ...

Specifies a variable argument list, which starts with an ANSI format string that describes the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".


## -remarks



To enable tracing in free builds, drivers must define the WIA_DEBUG macro by adding <code>#define WIA_DEBUG</code> before including any of the WIA headers. Tracing is enabled by default in checked and debug builds of the operating system.

The following is an example of how the macro would be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WIAS_TRACE((g_hInst,"WIA storage path = %ws",m_wszStoragePath));</pre>
</td>
</tr>
</table></span></div>
This code snippet was taken from <i>Wiadriver.cpp</i>, which is included with the WDK.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549531">WIAS_ASSERT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549565">WIAS_ERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a>
 

 

