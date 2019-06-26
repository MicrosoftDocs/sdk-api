---
UID: NF:immdev.ImmCreateContext
title: ImmCreateContext function (immdev.h)
author: windows-sdk-content
description: Creates a new input context, allocating memory for the context and initializing it. An application calls this function to prepare its own input context.
old-location: intl\immcreatecontext.htm
tech.root: Intl
ms.assetid: 2207927a-0edb-4d3a-a1b7-75b94d1616d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImmCreateContext, ImmCreateContext function [Internationalization for Windows Applications], _win32_ImmCreateContext, imm/ImmCreateContext, intl.immcreatecontext
ms.topic: function
f1_keywords: 
 - "immdev/ImmCreateContext"
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
 - ImmCreateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ImmCreateContext function


## -description


Creates a new input context, allocating memory for the context and initializing it. An application calls this function to prepare its own input context.


## -parameters






## -returns



Returns the handle to the new input context if successful, or <b>NULL</b> otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
 

 

