---
UID: NF:wmsdkidl.IWMReaderAdvanced.NotifyLateDelivery
title: IWMReaderAdvanced::NotifyLateDelivery (wmsdkidl.h)
description: The NotifyLateDelivery method is used to notify the reader that it is delivering data to the application too slowly.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","NotifyLateDelivery method","IWMReaderAdvanced.NotifyLateDelivery","IWMReaderAdvanced::NotifyLateDelivery","IWMReaderAdvancedNotifyLateDelivery","NotifyLateDelivery","NotifyLateDelivery method [windows Media Format]","NotifyLateDelivery method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_notifylatedelivery","wmsdkidl/IWMReaderAdvanced::NotifyLateDelivery"]
old-location: wmformat\iwmreaderadvanced_notifylatedelivery.htm
tech.root: wmformat
ms.assetid: 65d2470c-e6ce-4f3f-b4f8-0bc65a2a8bfd
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],NotifyLateDelivery method, IWMReaderAdvanced.NotifyLateDelivery, IWMReaderAdvanced::NotifyLateDelivery, IWMReaderAdvancedNotifyLateDelivery, NotifyLateDelivery, NotifyLateDelivery method [windows Media Format], NotifyLateDelivery method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_notifylatedelivery, wmsdkidl/IWMReaderAdvanced::NotifyLateDelivery
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
 - IWMReaderAdvanced::NotifyLateDelivery
 - wmsdkidl/IWMReaderAdvanced::NotifyLateDelivery
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
 - IWMReaderAdvanced.NotifyLateDelivery
---

# IWMReaderAdvanced::NotifyLateDelivery


## -description

The <b>NotifyLateDelivery</b> method is used to notify the reader that it is delivering data to the application too slowly.

## -parameters

### -param cnsLateness [in]

<b>QWORD</b> indicating how late the data is, in 100-nanosecond units.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>