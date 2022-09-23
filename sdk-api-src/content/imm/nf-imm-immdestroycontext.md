---
UID: NF:imm.ImmDestroyContext
title: ImmDestroyContext function (imm.h)
description: The ImmDestroyContext function (imm.h) releases the input context and frees associated memory.
helpviewer_keywords: ["ImmDestroyContext","ImmDestroyContext function [Internationalization for Windows Applications]","_win32_ImmDestroyContext","imm/ImmDestroyContext","intl.immdestroycontext"]
old-location: intl\immdestroycontext.htm
tech.root: Intl
ms.assetid: ab6dc79f-3c47-4ab0-ba72-1e7db7a72116
ms.date: 08/04/2022
ms.keywords: ImmDestroyContext, ImmDestroyContext function [Internationalization for Windows Applications], _win32_ImmDestroyContext, imm/ImmDestroyContext, intl.immdestroycontext
req.header: imm.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmDestroyContext
 - imm/ImmDestroyContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - ImmDestroyContext
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

Any application that creates an input context by using the <a href="/windows/desktop/api/imm/nf-imm-immcreatecontext">ImmCreateContext</a> function must call this function to free the context before it terminates. However, before calling <b>ImmDestroyContext</b>, the application must remove the input context from any association with windows in the thread by using the <a href="/windows/desktop/api/imm/nf-imm-immassociatecontext">ImmAssociateContext</a> function.

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immassociatecontext">ImmAssociateContext</a>



<a href="/windows/desktop/api/imm/nf-imm-immcreatecontext">ImmCreateContext</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
