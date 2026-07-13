---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnTime
title: IWMReaderCallbackAdvanced::OnTime (wmsdkidl.h)
description: The OnTime method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.
helpviewer_keywords: ["IWMReaderCallbackAdvanced interface [windows Media Format]","OnTime method","IWMReaderCallbackAdvanced.OnTime","IWMReaderCallbackAdvanced::OnTime","IWMReaderCallbackAdvancedOnTime","OnTime","OnTime method [windows Media Format]","OnTime method [windows Media Format]","IWMReaderCallbackAdvanced interface","wmformat.iwmreadercallbackadvanced_ontime","wmsdkidl/IWMReaderCallbackAdvanced::OnTime"]
old-location: wmformat\iwmreadercallbackadvanced_ontime.htm
tech.root: wmformat
ms.assetid: 9913bbc4-df59-484f-b050-324e2ecdeb1c
ms.date: 4/26/2023
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnTime method, IWMReaderCallbackAdvanced.OnTime, IWMReaderCallbackAdvanced::OnTime, IWMReaderCallbackAdvancedOnTime, OnTime, OnTime method [windows Media Format], OnTime method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_ontime, wmsdkidl/IWMReaderCallbackAdvanced::OnTime
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderCallbackAdvanced::OnTime
 - wmsdkidl/IWMReaderCallbackAdvanced::OnTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderCallbackAdvanced.OnTime
---

# IWMReaderCallbackAdvanced::OnTime


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnTime</b> method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.

## -parameters

### -param cnsCurrentTime [in]

<b>QWORD</b> containing the current time in 100-nanosecond units.

### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.

## -returns

To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="/windows/desktop/wmformat/error-codes">Error Codes</a>.

## -remarks

There are two cases in which callbacks indicating what the reader registers as the current elapsed time must be received by an application. The first case occurs when there are gaps in an ASF file (for example, no audio for 10 seconds). The <b>OnTime</b> method continues to be called, while <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">OnSample</a> does not. In the second case, if the application is driving the clock, the reader calls <b>OnTime</b> after it has delivered all the data up to the point requested by the application in a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime">IWMReaderAdvanced::DeliverTime</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>