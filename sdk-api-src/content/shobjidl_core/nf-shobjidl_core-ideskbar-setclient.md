---
UID: NF:shobjidl_core.IDeskBar.SetClient
title: IDeskBar::SetClient (shobjidl_core.h)
description: Sets the client specified by punkClient.
helpviewer_keywords: ["IDeskBar interface [Windows Shell]","SetClient method","IDeskBar.SetClient","IDeskBar::SetClient","SetClient","SetClient method [Windows Shell]","SetClient method [Windows Shell]","IDeskBar interface","_win32_IDeskBar_SetClient","shell.IDeskBar_SetClient","shobjidl_core/IDeskBar::SetClient"]
old-location: shell\IDeskBar_SetClient.htm
tech.root: shell
ms.assetid: 26655738-a2d5-446c-af7f-866b34beb3ab
ms.date: 12/05/2018
ms.keywords: IDeskBar interface [Windows Shell],SetClient method, IDeskBar.SetClient, IDeskBar::SetClient, SetClient, SetClient method [Windows Shell], SetClient method [Windows Shell],IDeskBar interface, _win32_IDeskBar_SetClient, shell.IDeskBar_SetClient, shobjidl_core/IDeskBar::SetClient
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDeskBar::SetClient
 - shobjidl_core/IDeskBar::SetClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDeskBar.SetClient
---

# IDeskBar::SetClient


## -description

Sets the client specified by <i>punkClient</i>.

## -parameters

### -param punkClient [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to a variable of type <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that specifies the client used by the desk bar.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.