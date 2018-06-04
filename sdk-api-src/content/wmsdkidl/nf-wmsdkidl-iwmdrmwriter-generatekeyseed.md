---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMDRMWriter::GenerateKeySeed


## -description


<p class="CCE_Message">[<b>GenerateKeySeed</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>GenerateKeySeed</b> method generates a <a href="wmformat_glossary.htm">DRM</a> key seed.




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
 

 

