---
UID: NF:imm.ImmDestroyContext
title: ImmDestroyContext function
author: windows-sdk-content
description: Releases the input context and frees associated memory.
old-location: intl\immdestroycontext.htm
tech.root: Intl
ms.assetid: ab6dc79f-3c47-4ab0-ba72-1e7db7a72116
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ImmDestroyContext, ImmDestroyContext function [Internationalization for Windows Applications], _win32_ImmDestroyContext, imm/ImmDestroyContext, intl.immdestroycontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - ImmDestroyContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmDestroyContext function


## -description


Releases the input context and frees associated memory.


## -parameters




### -param HIMC [in]

Handle to the input context to free.


## -returns



Returns a nonzero value if successful, or 0 otherwise.




## -remarks



Any application that creates an input context by using the <a href="https://msdn.microsoft.com/2207927a-0edb-4d3a-a1b7-75b94d1616d5">ImmCreateContext</a> function must call this function to free the context before it terminates. However, before calling <b>ImmDestroyContext</b>, the application must remove the input context from any association with windows in the thread by using the <a href="https://msdn.microsoft.com/978ea304-c44d-4f00-b86f-932bbd5f603c">ImmAssociateContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/978ea304-c44d-4f00-b86f-932bbd5f603c">ImmAssociateContext</a>



<a href="https://msdn.microsoft.com/2207927a-0edb-4d3a-a1b7-75b94d1616d5">ImmCreateContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

