---
UID: NF:wmsdkidl.IWMDRMWriter.GenerateKeySeed
title: IWMDRMWriter::GenerateKeySeed (wmsdkidl.h)
description: The GenerateKeySeed method generates a DRM key seed.
helpviewer_keywords: ["GenerateKeySeed","GenerateKeySeed method [windows Media Format]","GenerateKeySeed method [windows Media Format]","IWMDRMWriter interface","IWMDRMWriter interface [windows Media Format]","GenerateKeySeed method","IWMDRMWriter.GenerateKeySeed","IWMDRMWriter::GenerateKeySeed","IWMDRMWriterGenerateKeySeed","wmformat.iwmdrmwriter_generatekeyseed","wmsdkidl/IWMDRMWriter::GenerateKeySeed"]
old-location: wmformat\iwmdrmwriter_generatekeyseed.htm
tech.root: wmformat
ms.assetid: c3664dec-5ba4-4842-80f1-6652d526295d
ms.date: 12/05/2018
ms.keywords: GenerateKeySeed, GenerateKeySeed method [windows Media Format], GenerateKeySeed method [windows Media Format],IWMDRMWriter interface, IWMDRMWriter interface [windows Media Format],GenerateKeySeed method, IWMDRMWriter.GenerateKeySeed, IWMDRMWriter::GenerateKeySeed, IWMDRMWriterGenerateKeySeed, wmformat.iwmdrmwriter_generatekeyseed, wmsdkidl/IWMDRMWriter::GenerateKeySeed
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
 - IWMDRMWriter::GenerateKeySeed
 - wmsdkidl/IWMDRMWriter::GenerateKeySeed
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
 - IWMDRMWriter.GenerateKeySeed
---

# IWMDRMWriter::GenerateKeySeed


## -description

<p class="CCE_Message">[<b>GenerateKeySeed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GenerateKeySeed</b> method generates a <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> key seed.

## -parameters

### -param pwszKeySeed [out]

Pointer to a wide-character <b>null</b>-terminated string containing the key seed. Set to <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcwchLength</i>.

### -param pcwchLength [in, out]

Pointer to a <b>DWORD</b> containing the size, in wide characters, of <i>pwszKeySeed</i>. This size includes the terminating <b>null</b> character.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used infrequently because the same key seed should be used for multiple files. You can use the same key seed for every file created by an application, or distributed from the same server, or you can use it for some subset of files.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter Interface</a>