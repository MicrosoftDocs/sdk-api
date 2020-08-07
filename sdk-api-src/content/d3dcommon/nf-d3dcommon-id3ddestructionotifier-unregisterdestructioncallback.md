---
UID: NF:d3dcommon.ID3DDestructionNotifier.UnregisterDestructionCallback
title: ID3DDestructionNotifier::UnregisterDestructionCallback (d3dcommon.h)
description: Unregisters a callback registered with ID3DDestructionNotifier::RegisterDestructionCallback.
helpviewer_keywords: ["ID3DDestructionNotifier interface [Direct3D]","UnregisterDestructionCallback method","ID3DDestructionNotifier.UnregisterDestructionCallback","ID3DDestructionNotifier::UnregisterDestructionCallback","UnregisterDestructionCallback","UnregisterDestructionCallback method [Direct3D]","UnregisterDestructionCallback method [Direct3D]","ID3DDestructionNotifier interface","d3dcommon/ID3DDestructionNotifier::UnregisterDestructionCallback","direct3d11.id3ddestructionnotifier_unregisterdestructioncallback"]
old-location: direct3d11\id3ddestructionnotifier_unregisterdestructioncallback.htm
tech.root: direct3d11
ms.assetid: 4d10c986-1cba-427c-ae90-f81b83be1b8b
ms.date: 12/05/2018
ms.keywords: ID3DDestructionNotifier interface [Direct3D],UnregisterDestructionCallback method, ID3DDestructionNotifier.UnregisterDestructionCallback, ID3DDestructionNotifier::UnregisterDestructionCallback, UnregisterDestructionCallback, UnregisterDestructionCallback method [Direct3D], UnregisterDestructionCallback method [Direct3D],ID3DDestructionNotifier interface, d3dcommon/ID3DDestructionNotifier::UnregisterDestructionCallback, direct3d11.id3ddestructionnotifier_unregisterdestructioncallback
f1_keywords:
- d3dcommon/ID3DDestructionNotifier.UnregisterDestructionCallback
dev_langs:
- c++
req.header: d3dcommon.h
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
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3DCommon.h
api_name:
- ID3DDestructionNotifier.UnregisterDestructionCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3DDestructionNotifier::UnregisterDestructionCallback


## -description


Unregisters a callback registered with <b><a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-registerdestructioncallback"></b>.


## -parameters



### -param callbackID

Type: <b><a href="windows/desktop/WinProg/windows-data-types">UINT</a></b>

A **UINT** that was created by the **pCallbackID** parameter of <b><a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-registerdestructioncallback">ID3DDestructionNotifier::RegisterDestructionCallback</a></b>.
 


## -returns

Type: <b><a href="windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function suceeds, it will return **S_OK**

## -see-also




<a href="windows/desktop/api/d3dcommon/nn-d3dcommon-id3ddestructionnotifier">ID3DDestructionNotifier</a>



<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-registerdestructioncallback">ID3DDestructionNotifier::RegisterDestructionCallback</a>
 

 

