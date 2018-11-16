---
UID: NF:shobjidl_core.IInitializeWithBindCtx.Initialize
title: IInitializeWithBindCtx::Initialize
author: windows-sdk-content
description: Initializes a handler with a bind context.
old-location: shell\IInitializeWithBindCtx_Initialize.htm
tech.root: shell
ms.assetid: 5cb3117f-7e9f-463f-806c-4955cebc1c2d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IInitializeWithBindCtx interface [Windows Shell],Initialize method, IInitializeWithBindCtx.Initialize, IInitializeWithBindCtx::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithBindCtx interface, _shell_IInitializeWithBindCtx_Initialize, shell.IInitializeWithBindCtx_Initialize, shobjidl_core/IInitializeWithBindCtx::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithBindCtx.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IInitializeWithBindCtx.Initialize
: 
---

# IInitializeWithBindCtx::Initialize


## -description


Initializes a handler with a bind context.


## -parameters




### -param pbc [in]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



