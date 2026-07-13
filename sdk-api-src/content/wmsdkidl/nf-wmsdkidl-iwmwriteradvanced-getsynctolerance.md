---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetSyncTolerance
title: IWMWriterAdvanced::GetSyncTolerance (wmsdkidl.h)
description: The GetSyncTolerance method retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.
helpviewer_keywords: ["GetSyncTolerance","GetSyncTolerance method [windows Media Format]","GetSyncTolerance method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetSyncTolerance method","IWMWriterAdvanced.GetSyncTolerance","IWMWriterAdvanced::GetSyncTolerance","IWMWriterAdvancedGetSyncTolerance","wmformat.iwmwriteradvanced_getsynctolerance","wmsdkidl/IWMWriterAdvanced::GetSyncTolerance"]
old-location: wmformat\iwmwriteradvanced_getsynctolerance.htm
tech.root: wmformat
ms.assetid: f62d3405-3125-4df6-bd06-fa70358560ad
ms.date: 4/26/2023
ms.keywords: GetSyncTolerance, GetSyncTolerance method [windows Media Format], GetSyncTolerance method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetSyncTolerance method, IWMWriterAdvanced.GetSyncTolerance, IWMWriterAdvanced::GetSyncTolerance, IWMWriterAdvancedGetSyncTolerance, wmformat.iwmwriteradvanced_getsynctolerance, wmsdkidl/IWMWriterAdvanced::GetSyncTolerance
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
 - IWMWriterAdvanced::GetSyncTolerance
 - wmsdkidl/IWMWriterAdvanced::GetSyncTolerance
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
 - IWMWriterAdvanced.GetSyncTolerance
---

# IWMWriterAdvanced::GetSyncTolerance


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetSyncTolerance</b> method retrieves the amount of time during which the inputs can fall out of synchronization before the samples are discarded.

## -parameters

### -param pmsWindow [in]

Pointer to the limit of the number of milliseconds that the inputs can be out of synchronization. Note that this parameter is in milliseconds and not 100-nanosecond units.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pmsWindow</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The default tolerance is 3000 milliseconds.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance">IWMWriterAdvanced::SetSyncTolerance</a>