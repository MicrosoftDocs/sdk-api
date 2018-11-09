---
UID: NF:winbase.RemoveSecureMemoryCacheCallback
title: RemoveSecureMemoryCacheCallback function
author: windows-sdk-content
description: Unregisters a callback function that was previously registered with the AddSecureMemoryCacheCallback function.
old-location: base\removesecurememorycachecallback.htm
tech.root: memory
ms.assetid: 8be6ff04-34c7-4942-a38c-507584c8bbeb
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: RemoveSecureMemoryCacheCallback, RemoveSecureMemoryCacheCallback function, base.removesecurememorycachecallback, winbase/RemoveSecureMemoryCacheCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - RemoveSecureMemoryCacheCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveSecureMemoryCacheCallback function


## -description


Unregisters a callback function that was previously registered with the <a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a> function.


## -parameters




### -param pfnCallBack [in]

A pointer to the application-defined <a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a> function to remove.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.




## -remarks



To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a>



<a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a>
 

 

