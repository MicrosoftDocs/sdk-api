---
UID: NF:wmsdkidl.IWMPlayerHook.PreDecode
title: IWMPlayerHook::PreDecode (wmsdkidl.h)
description: The PreDecode method is called by the reader object before a sample from the output to which the IWMPlayerHook interface is assigned is passed to the video processor for decoding.
helpviewer_keywords: ["IWMPlayerHook interface [windows Media Format]","PreDecode method","IWMPlayerHook.PreDecode","IWMPlayerHook::PreDecode","IWMPlayerHookPreDecode","PreDecode","PreDecode method [windows Media Format]","PreDecode method [windows Media Format]","IWMPlayerHook interface","wmformat.iwmplayerhook_predecode","wmsdkidl/IWMPlayerHook::PreDecode"]
old-location: wmformat\iwmplayerhook_predecode.htm
tech.root: wmformat
ms.assetid: 88a78360-3e67-4425-8c65-3f746c6c807d
ms.date: 12/05/2018
ms.keywords: IWMPlayerHook interface [windows Media Format],PreDecode method, IWMPlayerHook.PreDecode, IWMPlayerHook::PreDecode, IWMPlayerHookPreDecode, PreDecode, PreDecode method [windows Media Format], PreDecode method [windows Media Format],IWMPlayerHook interface, wmformat.iwmplayerhook_predecode, wmsdkidl/IWMPlayerHook::PreDecode
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK with update number 888656 installed, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPlayerHook::PreDecode
 - wmsdkidl/IWMPlayerHook::PreDecode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMPlayerHook.PreDecode
---

# IWMPlayerHook::PreDecode


## -description

The <b>PreDecode</b> method is called by the reader object before a sample from the output to which the <b>IWMPlayerHook</b> interface is assigned is passed to the video processor for decoding.



## -returns

The method returns an <b>HRESULT</b>. You should return S_OK.

## -remarks

To assign an implementation of the <b>IWMPlayerHook</b> interface to an output in the reader object, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced5-setplayerhook">IWMReaderAdvanced5::SetPlayerHook</a>.

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook">IWMPlayerHook Interface</a>
