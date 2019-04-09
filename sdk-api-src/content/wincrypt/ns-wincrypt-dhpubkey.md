---
UID: NS:wincrypt._PUBKEY
title: DHPUBKEY (wincrypt.h)
author: windows-sdk-content
description: Contains information specific to the particular Diffie-Hellman public key contained in the key BLOB.
old-location: security\dhpubkey.htm
tech.root: SecCrypto
ms.assetid: 12fb2e81-796d-4501-91b5-ee572a3293bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DHPUBKEY, DHPUBKEY structure [Security], DSSPUBKEY, KEAPUBKEY, TEKPUBKEY, _PUBKEY, _crypto2_dhpubkey, security.dhpubkey, wincrypt/DHPUBKEY
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - DHPUBKEY
product: Windows
targetos: Windows
req.typenames: DHPUBKEY, DSSPUBKEY, KEAPUBKEY, TEKPUBKEY
req.redist: 
---

# DHPUBKEY structure


## -description


The <b>DHPUBKEY</b> structure contains information specific to the particular Diffie-Hellman <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> contained in the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>.


## -struct-fields




### -field magic

This must always be set to DH1 (0x31484400) when used for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key BLOBs</a> and to DH2 (0x32484400) when used for <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key BLOBs</a>. 




Notice that the hexadecimal values are simply an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> encoding of DH1 and DH2.


### -field bitlen

Number of bits in the prime modulus, P.


## -remarks



<b>DSSPUBKEY</b> is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">PUBLICKEYSTRUC</a>
 

 

