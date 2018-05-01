---
UID: NF:wiamdef.WIAS_ASSERT
title: WIAS_ASSERT macro
author: windows-driver-content
description: The WIAS_ASSERT macro writes a diagnostic message to the Wiatrace.log file.
old-location: image\wias_assert.htm
old-project: image
ms.assetid: 74dac8e1-a909-4c22-a650-af8a43421c5c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog_91198444-77d8-4f41-957b-de4c3262988a.xml, WIAS_ASSERT, WIAS_ASSERT macro [Imaging Devices], image.wias_assert, wiamdef/WIAS_ASSERT
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
-	WIAS_ASSERT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WIAS_ASSERT macro


## -description


The WIAS_ASSERT macro writes a diagnostic message to the <i>Wiatrace.log</i> file.


## -parameters




### -param x

TBD


### -param y

TBD






#### - Expression

Specifies any logical expression.


#### - HInst

Handle to the DLL (driver).


## -remarks



The WIAS_ASSERT macro is used to debug WIA drivers. It is used to test that a certain condition is met. If the <i>Expression</i> parameter evaluates to <b>TRUE</b>, this macro does nothing. If <i>Expression</i> evaluates to <b>FALSE</b>, the macro prints an error string to the <i>Wiatrace.log</i> diagnostic log file. This error message will contain the name and path to the calling driver and the line number in the driver source code where the WIAS_ASSERT macro failed.

The WIAS_ASSERT macro is available in Windows Vista and later versions of the operating system. This macro is the recommended way to implement WIA assertions on Windows Vista. WIAS_ASSERT allows error messages to be written to the log file (<i>Wiatrace.log</i>). The <i>Wiatrace.log</i> file is only available in Windows Vista, and later versions of the operating system. The utility used to view the contents of this log file is WiaTrcVw.exe.

To enable asserts in free builds, drivers must define the WIA_DEBUG macro by adding <code>#define WIA_DEBUG</code> to the driver's source code; this must be done before including any of the WIA headers. Asserts are enabled by default in checked and debug builds of the operating system.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549565">WIAS_ERROR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549572">WIAS_HRESULT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff549619">WIAS_TRACE</a>
 

 

