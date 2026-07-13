---
UID: NF:shobjidl.IEnumReadyCallback.EnumReady
title: IEnumReadyCallback::EnumReady (shobjidl.h)
description: Notifies the implementer that the view's item enumeration has completed.
helpviewer_keywords: ["EnumReady","EnumReady method [Windows Shell]","EnumReady method [Windows Shell]","IEnumReadyCallback interface","IEnumReadyCallback interface [Windows Shell]","EnumReady method","IEnumReadyCallback.EnumReady","IEnumReadyCallback::EnumReady","_shell_IEnumReadyCallback_EnumReady","shell.IEnumReadyCallback_EnumReady","shobjidl/IEnumReadyCallback::EnumReady"]
old-location: shell\IEnumReadyCallback_EnumReady.htm
tech.root: shell
ms.assetid: 4bb0772a-a863-49eb-a262-755d0ea3ea86
ms.date: 12/05/2018
ms.keywords: EnumReady, EnumReady method [Windows Shell], EnumReady method [Windows Shell],IEnumReadyCallback interface, IEnumReadyCallback interface [Windows Shell],EnumReady method, IEnumReadyCallback.EnumReady, IEnumReadyCallback::EnumReady, _shell_IEnumReadyCallback_EnumReady, shell.IEnumReadyCallback_EnumReady, shobjidl/IEnumReadyCallback::EnumReady
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumReadyCallback::EnumReady
 - shobjidl/IEnumReadyCallback::EnumReady
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IEnumReadyCallback.EnumReady
---

# IEnumReadyCallback::EnumReady


## -description

Notifies the implementer that the view's item enumeration has completed.  This callback interface is provided to the view via <a href="/windows/desktop/api/shobjidl/nf-shobjidl-ienumerableview-setenumreadycallback">SetEnumReadyCallback</a>



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
