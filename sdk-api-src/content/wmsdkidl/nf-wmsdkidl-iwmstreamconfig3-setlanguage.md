---
UID: NF:wmsdkidl.IWMStreamConfig3.SetLanguage
title: IWMStreamConfig3::SetLanguage (wmsdkidl.h)
description: The SetLanguage method sets the language for a stream using an RFC1766-compliant string.
helpviewer_keywords: ["IWMStreamConfig3 interface [windows Media Format]","SetLanguage method","IWMStreamConfig3.SetLanguage","IWMStreamConfig3::SetLanguage","IWMStreamConfig3SetLanguage","SetLanguage","SetLanguage method [windows Media Format]","SetLanguage method [windows Media Format]","IWMStreamConfig3 interface","wmformat.iwmstreamconfig3_setlanguage","wmsdkidl/IWMStreamConfig3::SetLanguage"]
old-location: wmformat\iwmstreamconfig3_setlanguage.htm
tech.root: wmformat
ms.assetid: 3d5c65b1-5e8b-4ee7-b28c-a35376c91ac4
ms.date: 4/26/2023
ms.keywords: IWMStreamConfig3 interface [windows Media Format],SetLanguage method, IWMStreamConfig3.SetLanguage, IWMStreamConfig3::SetLanguage, IWMStreamConfig3SetLanguage, SetLanguage, SetLanguage method [windows Media Format], SetLanguage method [windows Media Format],IWMStreamConfig3 interface, wmformat.iwmstreamconfig3_setlanguage, wmsdkidl/IWMStreamConfig3::SetLanguage
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
 - IWMStreamConfig3::SetLanguage
 - wmsdkidl/IWMStreamConfig3::SetLanguage
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
 - IWMStreamConfig3.SetLanguage
---

# IWMStreamConfig3::SetLanguage


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetLanguage</b> method sets the language for a stream using an RFC1766-compliant string.

## -parameters

### -param pwszLanguageString [in]

Pointer to a wide-character null-terminated string containing the language string.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The string passed to this method must be an RFC1766-compliant string. Use of other strings will cause problems when streaming a file made with this profile. For a list of commonly used language strings, see <a href="/windows/desktop/wmformat/language-strings">Language Strings</a>.

The new value will not take effect in the profile until you call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-getlanguage">IWMStreamConfig3::GetLanguage</a>