---
UID: NF:wmsdkidl.IWMWriterAdvanced.SetLiveSource
title: IWMWriterAdvanced::SetLiveSource (wmsdkidl.h)
description: The SetLiveSource method sets a flag indicating whether the source is live.
helpviewer_keywords: ["IWMWriterAdvanced interface [windows Media Format]","SetLiveSource method","IWMWriterAdvanced.SetLiveSource","IWMWriterAdvanced::SetLiveSource","IWMWriterAdvancedSetLiveSource","SetLiveSource","SetLiveSource method [windows Media Format]","SetLiveSource method [windows Media Format]","IWMWriterAdvanced interface","wmformat.iwmwriteradvanced_setlivesource","wmsdkidl/IWMWriterAdvanced::SetLiveSource"]
old-location: wmformat\iwmwriteradvanced_setlivesource.htm
tech.root: wmformat
ms.assetid: ab015f92-498e-44c7-95c9-869dfdfccc09
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced interface [windows Media Format],SetLiveSource method, IWMWriterAdvanced.SetLiveSource, IWMWriterAdvanced::SetLiveSource, IWMWriterAdvancedSetLiveSource, SetLiveSource, SetLiveSource method [windows Media Format], SetLiveSource method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_setlivesource, wmsdkidl/IWMWriterAdvanced::SetLiveSource
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
 - IWMWriterAdvanced::SetLiveSource
 - wmsdkidl/IWMWriterAdvanced::SetLiveSource
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
 - IWMWriterAdvanced.SetLiveSource
---

# IWMWriterAdvanced::SetLiveSource


## -description

The <b>SetLiveSource</b> method sets a flag indicating whether the source is live.

## -parameters

### -param fIsLiveSource [in]

Boolean value that is True if the source is live.

## -returns

This method always returns S_OK.

## -remarks

The default is False. To handle incoming samples correctly, the writer object must be notified whether the source is live.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>