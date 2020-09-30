---
UID: NF:shobjidl_core.IDeskBar.GetClient
title: IDeskBar::GetClient (shobjidl_core.h)
description: Gets the client object.
helpviewer_keywords: ["GetClient","GetClient method [Windows Shell]","GetClient method [Windows Shell]","IDeskBar interface","IDeskBar interface [Windows Shell]","GetClient method","IDeskBar.GetClient","IDeskBar::GetClient","_win32_IDeskBar_GetClient","shell.IDeskBar_GetClient","shobjidl_core/IDeskBar::GetClient"]
old-location: shell\IDeskBar_GetClient.htm
tech.root: shell
ms.assetid: 003b400c-03a4-47c0-a6b8-04aa65ac573c
ms.date: 12/05/2018
ms.keywords: GetClient, GetClient method [Windows Shell], GetClient method [Windows Shell],IDeskBar interface, IDeskBar interface [Windows Shell],GetClient method, IDeskBar.GetClient, IDeskBar::GetClient, _win32_IDeskBar_GetClient, shell.IDeskBar_GetClient, shobjidl_core/IDeskBar::GetClient
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
 - IDeskBar::GetClient
 - shobjidl_core/IDeskBar::GetClient
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
 - IDeskBar.GetClient
---

# IDeskBar::GetClient


## -description

Gets the client object.

## -parameters

### -param ppunkClient [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The address of a pointer to a variable of type <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that receives the client used by the desk bar.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the client object is returned, or an error value otherwise.