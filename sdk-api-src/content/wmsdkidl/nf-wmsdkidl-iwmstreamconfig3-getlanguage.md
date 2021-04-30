---
UID: NF:wmsdkidl.IWMStreamConfig3.GetLanguage
title: IWMStreamConfig3::GetLanguage (wmsdkidl.h)
description: The GetLanguage method retrieves the RFC1766-compliant language string for the stream.
helpviewer_keywords: ["GetLanguage","GetLanguage method [windows Media Format]","GetLanguage method [windows Media Format]","IWMStreamConfig3 interface","IWMStreamConfig3 interface [windows Media Format]","GetLanguage method","IWMStreamConfig3.GetLanguage","IWMStreamConfig3::GetLanguage","IWMStreamConfig3GetLanguage","wmformat.iwmstreamconfig3_getlanguage","wmsdkidl/IWMStreamConfig3::GetLanguage"]
old-location: wmformat\iwmstreamconfig3_getlanguage.htm
tech.root: wmformat
ms.assetid: 407607c8-c6ab-4400-b86c-9972d95f90c2
ms.date: 12/05/2018
ms.keywords: GetLanguage, GetLanguage method [windows Media Format], GetLanguage method [windows Media Format],IWMStreamConfig3 interface, IWMStreamConfig3 interface [windows Media Format],GetLanguage method, IWMStreamConfig3.GetLanguage, IWMStreamConfig3::GetLanguage, IWMStreamConfig3GetLanguage, wmformat.iwmstreamconfig3_getlanguage, wmsdkidl/IWMStreamConfig3::GetLanguage
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
 - IWMStreamConfig3::GetLanguage
 - wmsdkidl/IWMStreamConfig3::GetLanguage
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
 - IWMStreamConfig3.GetLanguage
---

# IWMStreamConfig3::GetLanguage


## -description

The <b>GetLanguage</b> method retrieves the RFC1766-compliant language string for the stream.

## -parameters

### -param pwszLanguageString [out]

Pointer to a wide-character <b>null</b>-terminated string containing the language string. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchLanguageStringLength</i>.

### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the size of the language string in wide characters. This size includes the terminating <b>null</b> character.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage">IWMStreamConfig3::SetLanguage</a>