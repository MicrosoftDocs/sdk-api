---
UID: NF:wmsdkidl.IWMWriterAdvanced.SetSyncTolerance
title: IWMWriterAdvanced::SetSyncTolerance (wmsdkidl.h)
description: The SetSyncTolerance method sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.
helpviewer_keywords: ["IWMWriterAdvanced interface [windows Media Format]","SetSyncTolerance method","IWMWriterAdvanced.SetSyncTolerance","IWMWriterAdvanced::SetSyncTolerance","IWMWriterAdvancedSetSyncTolerance","SetSyncTolerance","SetSyncTolerance method [windows Media Format]","SetSyncTolerance method [windows Media Format]","IWMWriterAdvanced interface","wmformat.iwmwriteradvanced_setsynctolerance","wmsdkidl/IWMWriterAdvanced::SetSyncTolerance"]
old-location: wmformat\iwmwriteradvanced_setsynctolerance.htm
tech.root: wmformat
ms.assetid: d60020bf-52f1-46a0-aeae-367e3b179fac
ms.date: 4/26/2023
ms.keywords: IWMWriterAdvanced interface [windows Media Format],SetSyncTolerance method, IWMWriterAdvanced.SetSyncTolerance, IWMWriterAdvanced::SetSyncTolerance, IWMWriterAdvancedSetSyncTolerance, SetSyncTolerance, SetSyncTolerance method [windows Media Format], SetSyncTolerance method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_setsynctolerance, wmsdkidl/IWMWriterAdvanced::SetSyncTolerance
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
 - IWMWriterAdvanced::SetSyncTolerance
 - wmsdkidl/IWMWriterAdvanced::SetSyncTolerance
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
 - IWMWriterAdvanced.SetSyncTolerance
---

# IWMWriterAdvanced::SetSyncTolerance


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetSyncTolerance</b> method sets the amount of time that the inputs can fall out of synchronization before the samples are discarded.

## -parameters

### -param msWindow [in]

Amount of time that the inputs can be out of synchronization, in milliseconds. Note that this parameter is in milliseconds and not 100-nanosecond units.

## -returns

This method always returns S_OK.

## -remarks

The default tolerance value is 3000 milliseconds.

Regardless of what the tolerance is set to, keeping samples as tightly synchronized as possible results in the best performance and the highest-quality content.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsynctolerance">IWMWriterAdvanced::GetSyncTolerance</a>