---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Encrypt
title: IWMSecureChannel::WMSC_Encrypt (wmsecure.h)
author: windows-sdk-content
description: The WMSC_Encrypt method encrypts data across DLL boundaries.
old-location: wmformat\iwmsecurechannel_wmsc_encrypt.htm
tech.root: wmformat
ms.assetid: fdb90fbc-9504-4b72-83ab-b410c3bd2e1e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Encrypt method, IWMSecureChannel.WMSC_Encrypt, IWMSecureChannel::WMSC_Encrypt, WMSC_Encrypt, WMSC_Encrypt method [windows Media Format], WMSC_Encrypt method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_encrypt, wmsecure/IWMSecureChannel::WMSC_Encrypt
ms.topic: method
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMSecureChannel.WMSC_Encrypt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSecureChannel::WMSC_Encrypt


## -description


<p class="CCE_Message">[<b>WMSC_Encrypt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>WMSC_Encrypt</b> method encrypts data across DLL boundaries.


## -parameters




### -param pbData [in]


### -param cbData [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Encrypt</b> holds a lock on the connection which is released by <a href="https://msdn.microsoft.com/en-us/library/Dd743709(v=VS.85).aspx">Decrypt</a>, so threads should not block between calls to encrypt
     and decrypt.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743705(v=VS.85).aspx">IWMSecureChannel</a>
 

 

