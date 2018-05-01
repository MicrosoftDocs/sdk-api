---
UID: NF:wiautil.WIAS_ERROR
title: WIAS_ERROR macro
author: windows-driver-content
description: The WIAS_ERROR macro writes a diagnostic message to the Wiatrace.log file.
old-location: image\wias_error.htm
old-project: image
ms.assetid: e439f130-1b99-4f46-ace5-3456c09a5f67
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_5b3e0d61-e0e5-4385-8256-943e437cee9d.xml, WIAS_ERROR, WIAS_ERROR macro [Imaging Devices], image.wias_error, wiamdef/WIAS_ERROR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the operating system.
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
-	WIAS_ERROR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_ERROR macro


## -description


The WIAS_ERROR macro writes a diagnostic message to the <i>Wiatrace.log</i> file.


## -parameters




### -param x

TBD






#### - HInst

Handle to the DLL (driver).


####### - format_string, ...

Specifies a variable argument list, which starts with an ANSI format string that describes the message and any format identifiers. The ellipsis (...) specifies a variable number of arguments that need to be output. The error text should be prefixed with the full name of the method or function and generate the message in the format of "class::method, error-text".


## -remarks



This macro is the recommended way to implement error logging on Windows Vista, because unlike <a href="https://msdn.microsoft.com/library/windows/hardware/ff549580">WIAS_LERROR</a>, WIA_ERROR allows error messages to be written to the log file (<i>Wiatrace.log</i>). The <i>Wiatrace.log</i> file is only available in Windows Vista and later versions of the operating system. The utility used to view the contents of this log file is WiaTrcVw.exe.

To enable tracing in free builds, drivers must define the WIA_DEBUG macro by adding <code>#define WIA_DEBUG</code> before including any of the WIA headers. Tracing is enabled by default in checked and debug builds of the operating system.

The following is an example of how the macro can be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>WIAS_ERROR((g_hInst, "Failed to read (%ws) entry under %ws section of device registry",REG_ENTRY_STORAGEPATH,REG_ENTRY_DEVICEDATA));</pre>
</td>
</tr>
</table></span></div>
This code snippet was taken from <i>Wiadriver.cpp</i>, which is included with the WDK.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549531">WIAS_ASSERT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549619">WIAS_TRACE</a>
 

 

