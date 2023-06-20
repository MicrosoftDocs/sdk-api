---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnStreamSelection
title: IWMReaderCallbackAdvanced::OnStreamSelection (wmsdkidl.h)
description: The OnStreamSelection method notifies the application of stream changes made due to bandwidth restrictions. To have this method called, call IWMReaderAdvanced::SetReceiveSelectionCallbacks.
helpviewer_keywords: ["IWMReaderCallbackAdvanced interface [windows Media Format]","OnStreamSelection method","IWMReaderCallbackAdvanced.OnStreamSelection","IWMReaderCallbackAdvanced::OnStreamSelection","IWMReaderCallbackAdvancedOnStreamSelection","OnStreamSelection","OnStreamSelection method [windows Media Format]","OnStreamSelection method [windows Media Format]","IWMReaderCallbackAdvanced interface","wmformat.iwmreadercallbackadvanced_onstreamselection","wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSelection"]
old-location: wmformat\iwmreadercallbackadvanced_onstreamselection.htm
tech.root: wmformat
ms.assetid: d0d699b3-e2f3-427c-9159-e2ed875887ca
ms.date: 4/26/2023
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnStreamSelection method, IWMReaderCallbackAdvanced.OnStreamSelection, IWMReaderCallbackAdvanced::OnStreamSelection, IWMReaderCallbackAdvancedOnStreamSelection, OnStreamSelection, OnStreamSelection method [windows Media Format], OnStreamSelection method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_onstreamselection, wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSelection
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
 - IWMReaderCallbackAdvanced::OnStreamSelection
 - wmsdkidl/IWMReaderCallbackAdvanced::OnStreamSelection
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
 - IWMReaderCallbackAdvanced.OnStreamSelection
---

# IWMReaderCallbackAdvanced::OnStreamSelection


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>OnStreamSelection</b> method notifies the application of stream changes made due to bandwidth restrictions. To have this method called, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceiveselectioncallbacks">IWMReaderAdvanced::SetReceiveSelectionCallbacks</a>.

## -parameters

### -param wStreamCount [in]

<b>WORD</b> containing the number of entries in the <i>pStreamNumbers</i> array.

### -param pStreamNumbers [in]

Pointer to an array of stream numbers.

### -param pSelections [in]

Pointer to an array of members of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_stream_selection">WMT_STREAM_SELECTION</a> enumeration type. Each element in this array corresponds to the stream number contained in the corresponding element of the array pointed to by <i>pStreamNumbers</i>.

### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.

## -returns

To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="/windows/desktop/wmformat/error-codes">Error Codes</a>.

## -remarks

Stream numbers are in the range of 1 through 63.

The application can also get callbacks when stream changes due to bandwidth restrictions occur.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>