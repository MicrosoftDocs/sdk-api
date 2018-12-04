---
UID: NF:dbghelp.ImagehlpApiVersionEx
title: ImagehlpApiVersionEx function
author: windows-sdk-content
description: Modifies the version information of the library used by the application.
old-location: base\imagehlpapiversionex.htm
tech.root: debug
ms.assetid: 86a26160-ebad-4d6e-b559-3d59f2beb5ca
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ImagehlpApiVersionEx, ImagehlpApiVersionEx function, _win32_imagehlpapiversionex, base.imagehlpapiversionex, dbghelp/ImagehlpApiVersionEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - ImagehlpApiVersionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# ImagehlpApiVersionEx function


## -description


Modifies the version information of the library used by the application.


## -parameters




### -param AppVersion [in]

A pointer to an 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure that contains valid version information for your application.


## -returns



The return value is a pointer to an 
<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a> structure.
					




## -remarks



Use the 
<b>ImagehlpApiVersionEx</b> function to indicate the version of the library with which the application was built. The library uses this information to ensure compatibility. For example, consider walking through kernel-mode callback stack frames (User and GDI exist in kernel mode). If you call 
<b>ImagehlpApiVersionEx</b> to set the <b>Revision</b> member to version 4 or later, the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function will continue through a callback stack frame. Otherwise, if you set <b>Revision</b> to a version earlier than 4, 
<b>StackWalk64</b> will stop at the kernel transition.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/f983f639-6a94-4b83-a443-0d98b85d3950">API_VERSION</a>



<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/0ad9a047-f2ae-4fbe-8a85-9817a616ef73">ImagehlpApiVersion</a>
 

 

