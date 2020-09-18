---
UID: NF:wmsdkidl.IWMRegisterCallback.Unadvise
title: IWMRegisterCallback::Unadvise (wmsdkidl.h)
description: The Unadvise method unregisters the application's IWMStatusCallback callback interface. Call this method when the application has finished using the sink object. It notifies the object to stop sending status events to the application.
helpviewer_keywords: ["IWMRegisterCallback interface [windows Media Format]","Unadvise method","IWMRegisterCallback.Unadvise","IWMRegisterCallback::Unadvise","IWMRegisterCallbackUnadvise","Unadvise","Unadvise method [windows Media Format]","Unadvise method [windows Media Format]","IWMRegisterCallback interface","wmformat.iwmregistercallback_unadvise","wmsdkidl/IWMRegisterCallback::Unadvise"]
old-location: wmformat\iwmregistercallback_unadvise.htm
tech.root: wmformat
ms.assetid: 5f320288-09a8-4eaf-a7cd-54a4b52d0b47
ms.date: 12/05/2018
ms.keywords: IWMRegisterCallback interface [windows Media Format],Unadvise method, IWMRegisterCallback.Unadvise, IWMRegisterCallback::Unadvise, IWMRegisterCallbackUnadvise, Unadvise, Unadvise method [windows Media Format], Unadvise method [windows Media Format],IWMRegisterCallback interface, wmformat.iwmregistercallback_unadvise, wmsdkidl/IWMRegisterCallback::Unadvise
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IWMRegisterCallback::Unadvise
 - wmsdkidl/IWMRegisterCallback::Unadvise
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
 - IWMRegisterCallback.Unadvise
---

# IWMRegisterCallback::Unadvise


## -description

The <b>Unadvise</b> method unregisters the application's <b>IWMStatusCallback</b> callback interface. Call this method when the application has finished using the sink object. It notifies the object to stop sending status events to the application.

## -parameters

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface of an object.

### -param pvContext [in]

Generic pointer, for use by the application.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback">IWMRegisterCallback Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise">IWMRegisterCallback::Advise</a>