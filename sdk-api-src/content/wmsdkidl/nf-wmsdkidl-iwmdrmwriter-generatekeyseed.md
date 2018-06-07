---
UID: NF:wmsdkidl.IWMDRMWriter.GenerateKeySeed
title: IWMDRMWriter::GenerateKeySeed
author: windows-sdk-content
description: The GenerateKeySeed method generates a DRM key seed.
old-location: wmformat\iwmdrmwriter_generatekeyseed.htm
old-project: wmformat
ms.assetid: c3664dec-5ba4-4842-80f1-6652d526295d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GenerateKeySeed, GenerateKeySeed method [windows Media Format], GenerateKeySeed method [windows Media Format],IWMDRMWriter interface, IWMDRMWriter interface [windows Media Format],GenerateKeySeed method, IWMDRMWriter.GenerateKeySeed, IWMDRMWriter::GenerateKeySeed, IWMDRMWriterGenerateKeySeed, wmformat.iwmdrmwriter_generatekeyseed, wmsdkidl/IWMDRMWriter::GenerateKeySeed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMWriter::GenerateKeySeed


## -description


<p class="CCE_Message">[<b>GenerateKeySeed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GenerateKeySeed</b> method generates a <a href="https://docs.microsoft.com/windows/desktop//wmformat/wmformat-glossary">DRM</a> key seed.




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




<a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter Interface</a>
 

 

