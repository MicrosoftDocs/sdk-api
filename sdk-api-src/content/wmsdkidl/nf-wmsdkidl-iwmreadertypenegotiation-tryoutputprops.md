---
UID: NF:wmsdkidl.IWMReaderTypeNegotiation.TryOutputProps
title: IWMReaderTypeNegotiation::TryOutputProps (wmsdkidl.h)
description: The TryOutputProps method ascertains whether certain changes to the properties of an output are possible.
helpviewer_keywords: ["IWMReaderTypeNegotiation interface [windows Media Format]","TryOutputProps method","IWMReaderTypeNegotiation.TryOutputProps","IWMReaderTypeNegotiation::TryOutputProps","IWMReaderTypeNegotiationTryOutputProps","TryOutputProps","TryOutputProps method [windows Media Format]","TryOutputProps method [windows Media Format]","IWMReaderTypeNegotiation interface","wmformat.iwmreadertypenegotiation_tryoutputprops","wmsdkidl/IWMReaderTypeNegotiation::TryOutputProps"]
old-location: wmformat\iwmreadertypenegotiation_tryoutputprops.htm
tech.root: wmformat
ms.assetid: 87d16641-3d28-4bad-962b-8ec808cd7877
ms.date: 4/26/2023
ms.keywords: IWMReaderTypeNegotiation interface [windows Media Format],TryOutputProps method, IWMReaderTypeNegotiation.TryOutputProps, IWMReaderTypeNegotiation::TryOutputProps, IWMReaderTypeNegotiationTryOutputProps, TryOutputProps, TryOutputProps method [windows Media Format], TryOutputProps method [windows Media Format],IWMReaderTypeNegotiation interface, wmformat.iwmreadertypenegotiation_tryoutputprops, wmsdkidl/IWMReaderTypeNegotiation::TryOutputProps
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
 - IWMReaderTypeNegotiation::TryOutputProps
 - wmsdkidl/IWMReaderTypeNegotiation::TryOutputProps
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
 - IWMReaderTypeNegotiation.TryOutputProps
---

# IWMReaderTypeNegotiation::TryOutputProps


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>TryOutputProps</b> method ascertains whether certain changes to the properties of an output are possible.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param pOutput [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface of an output media properties object.

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
<i>dwOutputNumber</i> is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_OUTPUT_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
Media type of object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to complete the task.

</td>
</tr>
</table>

## -remarks

This method is usually used to test different output properties to find out if they are possible; for example, to find out whether a video stream can be rendered at a resolution of 320 x 240 pixels in 16-bit color. To perform this testing, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops">IWMReader::GetOutputProps</a> to retrieve an <b>IWMOutputMediaProps</b> interface, and alter properties by using that interface. Then test the modified object with the <b>TryOutputProps</b> method. If it returns S_OK, the new properties would work.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation">IWMReaderTypeNegotiation Interface</a>



<a href="/windows/desktop/wmformat/inputs-streams-and-outputs">Inputs, Streams and Outputs</a>