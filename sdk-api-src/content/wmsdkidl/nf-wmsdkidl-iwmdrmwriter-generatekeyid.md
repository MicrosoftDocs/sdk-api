---
UID: NF:wmsdkidl.IWMDRMWriter.GenerateKeyID
title: IWMDRMWriter::GenerateKeyID (wmsdkidl.h)
description: The GenerateKeyID method generates a DRM key ID.
helpviewer_keywords: ["GenerateKeyID","GenerateKeyID method [windows Media Format]","GenerateKeyID method [windows Media Format]","IWMDRMWriter interface","IWMDRMWriter interface [windows Media Format]","GenerateKeyID method","IWMDRMWriter.GenerateKeyID","IWMDRMWriter::GenerateKeyID","IWMDRMWriterGenerateKeyID","wmformat.iwmdrmwriter_generatekeyid","wmsdkidl/IWMDRMWriter::GenerateKeyID"]
old-location: wmformat\iwmdrmwriter_generatekeyid.htm
tech.root: wmformat
ms.assetid: 11eff02d-af0a-4047-80fd-d92be2f40d86
ms.date: 4/26/2023
ms.keywords: GenerateKeyID, GenerateKeyID method [windows Media Format], GenerateKeyID method [windows Media Format],IWMDRMWriter interface, IWMDRMWriter interface [windows Media Format],GenerateKeyID method, IWMDRMWriter.GenerateKeyID, IWMDRMWriter::GenerateKeyID, IWMDRMWriterGenerateKeyID, wmformat.iwmdrmwriter_generatekeyid, wmsdkidl/IWMDRMWriter::GenerateKeyID
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
 - IWMDRMWriter::GenerateKeyID
 - wmsdkidl/IWMDRMWriter::GenerateKeyID
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
 - IWMDRMWriter.GenerateKeyID
---

# IWMDRMWriter::GenerateKeyID


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GenerateKeyID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GenerateKeyID</b> method generates a DRM key ID.

## -parameters

### -param pwszKeyID [out]

Pointer to a wide-character <b>null</b>-terminated string containing the key identifier. Set to <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcwchLength</i>.

### -param pcwchLength [in, out]

Pointer to a <b>DWORD</b> containing the size, in wide characters, of <i>pwszKeyID</i>. This size includes the terminating <b>null</b> character.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Each file should have its own key ID.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter Interface</a>