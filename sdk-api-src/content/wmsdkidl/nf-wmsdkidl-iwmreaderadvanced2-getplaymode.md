---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetPlayMode
title: IWMReaderAdvanced2::GetPlayMode (wmsdkidl.h)
description: The GetPlayMode method retrieves the current play mode.
helpviewer_keywords: ["GetPlayMode","GetPlayMode method [windows Media Format]","GetPlayMode method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetPlayMode method","IWMReaderAdvanced2.GetPlayMode","IWMReaderAdvanced2::GetPlayMode","IWMReaderAdvanced2GetPlayMode","wmformat.iwmreaderadvanced2_getplaymode","wmsdkidl/IWMReaderAdvanced2::GetPlayMode"]
old-location: wmformat\iwmreaderadvanced2_getplaymode.htm
tech.root: wmformat
ms.assetid: 45c7e2c2-fff4-41a9-b5ce-76d8d6257e77
ms.date: 4/26/2023
ms.keywords: GetPlayMode, GetPlayMode method [windows Media Format], GetPlayMode method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetPlayMode method, IWMReaderAdvanced2.GetPlayMode, IWMReaderAdvanced2::GetPlayMode, IWMReaderAdvanced2GetPlayMode, wmformat.iwmreaderadvanced2_getplaymode, wmsdkidl/IWMReaderAdvanced2::GetPlayMode
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
 - IWMReaderAdvanced2::GetPlayMode
 - wmsdkidl/IWMReaderAdvanced2::GetPlayMode
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
 - IWMReaderAdvanced2.GetPlayMode
---

# IWMReaderAdvanced2::GetPlayMode


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPlayMode</b> method retrieves the current play mode.

## -parameters

### -param pMode [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_play_mode">WMT_PLAY_MODE</a> enumeration type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Before a file is opened, this method returns the play mode the reader will use to open a file. The default setting is auto-select (the reader picks the mode). After a file is opened, this method returns the actual mode used to play the file. For an asynchronous <b>Open</b> request, the actual mode can be obtained after receiving the WMT_OPENED status message.

For more information, see the Remarks section of <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode">IWMReaderAdvanced2::SetPlayMode</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>