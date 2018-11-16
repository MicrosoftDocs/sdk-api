---
UID: NF:wmsecure.IWMSecureChannel.WMSC_Decrypt
title: IWMSecureChannel::WMSC_Decrypt
author: windows-sdk-content
description: The WMSC_Decrypt method decrypts data across DLL boundaries.
old-location: wmformat\iwmsecurechannel_wmsc_decrypt.htm
tech.root: wmformat
ms.assetid: c477c1f9-0264-4d3f-8670-f0c52df9e6a6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMSecureChannel interface [windows Media Format],WMSC_Decrypt method, IWMSecureChannel.WMSC_Decrypt, IWMSecureChannel::WMSC_Decrypt, WMSC_Decrypt, WMSC_Decrypt method [windows Media Format], WMSC_Decrypt method [windows Media Format],IWMSecureChannel interface, wmformat.iwmsecurechannel_wmsc_decrypt, wmsecure/IWMSecureChannel::WMSC_Decrypt
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMSecureChannel.WMSC_Decrypt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsecure.h
: 
- IWMSecureChannel.WMSC_Decrypt
: 
---

# IWMSecureChannel::WMSC_Decrypt


## -description


<p class="CCE_Message">[<b>WMSC_Decrypt</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>WMSC_Decrypt</b> method decrypts data across DLL boundaries


## -parameters




### -param pbData [in]


### -param cbData [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




<a href="https://msdn.microsoft.com/fdb90fbc-9504-4b72-83ab-b410c3bd2e1e">Encrypt</a> holds a lock on the connection which is released by <b>Decrypt</b>, so threads should not block between calls to encrypt
     and decrypt.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

