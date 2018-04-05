---
UID: NF:wmsdkidl.IWMDRMWriter.GenerateKeyID
title: IWMDRMWriter::GenerateKeyID method
author: windows-driver-content
description: The GenerateKeyID method generates a DRM key ID.
old-location: wmformat\iwmdrmwriter_generatekeyid.htm
old-project: wmformat
ms.assetid: 11eff02d-af0a-4047-80fd-d92be2f40d86
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GenerateKeyID method [windows Media Format], GenerateKeyID method [windows Media Format], IWMDRMWriter interface, GenerateKeyID,IWMDRMWriter.GenerateKeyID, IWMDRMWriter, IWMDRMWriter interface [windows Media Format], GenerateKeyID method, IWMDRMWriter::GenerateKeyID, IWMDRMWriterGenerateKeyID, wmformat.iwmdrmwriter_generatekeyid, wmsdkidl/IWMDRMWriter::GenerateKeyID
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMDRMWriter.GenerateKeyID
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMWriter::GenerateKeyID method


## -description


<p class="CCE_Message">[<b>GenerateKeyID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
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




<a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter Interface</a>
 

 

