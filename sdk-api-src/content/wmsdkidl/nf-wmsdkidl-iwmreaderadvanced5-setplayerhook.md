---
UID: NF:wmsdkidl.IWMReaderAdvanced5.SetPlayerHook
title: IWMReaderAdvanced5::SetPlayerHook (wmsdkidl.h)
description: The SetPlayerHook method assigns a player-hook callback to the reader. The reader calls the callback method before sending each sample to the graphics processor for decompression.
helpviewer_keywords: ["IWMReaderAdvanced5 interface [windows Media Format]","SetPlayerHook method","IWMReaderAdvanced5.SetPlayerHook","IWMReaderAdvanced5::SetPlayerHook","IWMReaderAdvanced5SetPlayerHook","SetPlayerHook","SetPlayerHook method [windows Media Format]","SetPlayerHook method [windows Media Format]","IWMReaderAdvanced5 interface","wmformat.iwmreaderadvanced5_setplayerhook","wmsdkidl/IWMReaderAdvanced5::SetPlayerHook"]
old-location: wmformat\iwmreaderadvanced5_setplayerhook.htm
tech.root: wmformat
ms.assetid: 499c6c31-8cdf-4b99-964a-1fd51c14c5bd
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced5 interface [windows Media Format],SetPlayerHook method, IWMReaderAdvanced5.SetPlayerHook, IWMReaderAdvanced5::SetPlayerHook, IWMReaderAdvanced5SetPlayerHook, SetPlayerHook, SetPlayerHook method [windows Media Format], SetPlayerHook method [windows Media Format],IWMReaderAdvanced5 interface, wmformat.iwmreaderadvanced5_setplayerhook, wmsdkidl/IWMReaderAdvanced5::SetPlayerHook
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK with update number 888656 installed, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMReaderAdvanced5::SetPlayerHook
 - wmsdkidl/IWMReaderAdvanced5::SetPlayerHook
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
 - IWMReaderAdvanced5.SetPlayerHook
---

# IWMReaderAdvanced5::SetPlayerHook


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetPlayerHook</b> method assigns a player-hook callback to the reader. The reader calls the callback method before sending each sample to the graphics processor for decompression.

## -parameters

### -param dwOutputNum [in]

The output number to which the player-hook callback applies.

### -param pHook [in]

Pointer to the implementation of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook">IWMPlayerHook</a> interface that will be used in association with the specified output.

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
</table>

## -remarks

DirectX Video Acceleration enables supported graphics cards to decompress video samples.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5">IWMReaderAdvanced5 Interface</a>