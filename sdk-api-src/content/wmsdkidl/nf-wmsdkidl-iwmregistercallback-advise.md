---
UID: NF:wmsdkidl.IWMRegisterCallback.Advise
title: IWMRegisterCallback::Advise (wmsdkidl.h)
description: The Advise method registers the application to receive status messages from the sink object.
helpviewer_keywords: ["Advise","Advise method [windows Media Format]","Advise method [windows Media Format]","IWMRegisterCallback interface","IWMRegisterCallback interface [windows Media Format]","Advise method","IWMRegisterCallback.Advise","IWMRegisterCallback::Advise","IWMRegisterCallbackAdvise","wmformat.iwmregistercallback_advise","wmsdkidl/IWMRegisterCallback::Advise"]
old-location: wmformat\iwmregistercallback_advise.htm
tech.root: wmformat
ms.assetid: 69d12e5c-23fd-4d4b-959e-fe7979bf3fdb
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [windows Media Format], Advise method [windows Media Format],IWMRegisterCallback interface, IWMRegisterCallback interface [windows Media Format],Advise method, IWMRegisterCallback.Advise, IWMRegisterCallback::Advise, IWMRegisterCallbackAdvise, wmformat.iwmregistercallback_advise, wmsdkidl/IWMRegisterCallback::Advise
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
 - IWMRegisterCallback::Advise
 - wmsdkidl/IWMRegisterCallback::Advise
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
 - IWMRegisterCallback.Advise
---

# IWMRegisterCallback::Advise


## -description

The <b>Advise</b> method registers the application to receive status messages from the sink object.

## -parameters

### -param pCallback [in]

Pointer to the application's <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface. The application must implement this interface.

### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to <b>OnStatus</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The sink object sends status messages to the application by calling the application's <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method.

When the application has finished using the sink object, use the <b>Unadvise</b> method to break the connection with the sink object.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback">IWMRegisterCallback Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise">IWMRegisterCallback::Unadvise</a>