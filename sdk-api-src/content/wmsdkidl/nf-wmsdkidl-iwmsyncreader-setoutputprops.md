---
UID: NF:wmsdkidl.IWMSyncReader.SetOutputProps
title: IWMSyncReader::SetOutputProps (wmsdkidl.h)
description: The SetOutputProps method specifies the media properties of an uncompressed output stream.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","SetOutputProps method","IWMSyncReader.SetOutputProps","IWMSyncReader::SetOutputProps","IWMSyncReaderSetOutputProps","SetOutputProps","SetOutputProps method [windows Media Format]","SetOutputProps method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_setoutputprops","wmsdkidl/IWMSyncReader::SetOutputProps"]
old-location: wmformat\iwmsyncreader_setoutputprops.htm
tech.root: wmformat
ms.assetid: 5575fd7c-5eb0-4e4a-957d-e3fc174316ff
ms.date: 4/26/2023
ms.keywords: IWMSyncReader interface [windows Media Format],SetOutputProps method, IWMSyncReader.SetOutputProps, IWMSyncReader::SetOutputProps, IWMSyncReaderSetOutputProps, SetOutputProps, SetOutputProps method [windows Media Format], SetOutputProps method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setoutputprops, wmsdkidl/IWMSyncReader::SetOutputProps
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMSyncReader::SetOutputProps
 - wmsdkidl/IWMSyncReader::SetOutputProps
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
 - IWMSyncReader.SetOutputProps
---

# IWMSyncReader::SetOutputProps


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetOutputProps</b> method specifies the media properties of an uncompressed output stream.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param pOutput [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps</a> interface.

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
The <i>dwOutputNum</i> parameter is greater than or equal to the number of outputs. Output numbers begin with zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

Manipulating an object retrieved by a call to <b>GetOutputProps</b> has no effect on the output media stream unless the application also calls <b>SetOutputProps</b>.

DirectX VA formats can be returned from <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat">GetOutputFormat</a>, but if they are passed in to <b>SetOutputProps</b>, that method will fail because DirectX VA formats cannot be specified in this way. Therefore, your code should either examine the format before passing it to <b>SetOutputProps</b>, or else handle the case of that method failing by attempting the next format enumerated from <b>GetOutputFormat</b>.. For example code showing how to identify a DirectX VA format, see <a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>.

You can call <b>SetOutputProps</b> at any time after a file has been loaded into the synchronous reader. You can continue making calls as needed during playback.

New output properties set with this method will take effect with the next call to <b>GetNextSample</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops">IWMOutputMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops">IWMSyncReader::GetOutputProps</a>