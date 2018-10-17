---
UID: NS:wincrypt._PUBKEYVER3
title: "_PUBKEYVER3"
author: windows-sdk-content
description: Contains information specific to the particular public key contained in the key BLOB.
old-location: security\dhpubkey_ver3.htm
tech.root: seccrypto
ms.assetid: 02f702dd-be9d-4a9a-a3af-4db1802386b0
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: DHPUBKEY_VER3, DHPUBKEY_VER3 structure [Security], DSSPUBKEY_VER3, _PUBKEYVER3, _crypto2_dhpubkey_ver3, security.dhpubkey_ver3, wincrypt/DHPUBKEY_VER3
ms.prod: windows
ms.technology: windows-sdk
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
 - DHPUBKEY_VER3
product: Windows
targetos: Windows
req.typenames: DHPUBKEY_VER3, DSSPUBKEY_VER3
req.redist: 
---

# _PUBKEYVER3 structure


## -description


The <b>DHPUBKEY_VER3</b> structure contains information specific to the particular <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> contained in the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>.


## -struct-fields




### -field magic

This must always be set to 0x33484400, the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> encoding of "DH3".


### -field bitlenP

Number of bits in the DH key BLOB's prime, P.


### -field bitlenQ

Number of bits in the DH key BLOB's prime, Q. If Q is not available, then this value should be 0.


### -field bitlenJ

Number of bits in the DH key BLOB's prime, J. If J is not in the BLOB, then this value should be 0.


### -field DSSSeed

Seed structure holding the seed and counter values used to generate the primes Q and P. If values in the <a href="https://msdn.microsoft.com/fbf2b5e4-b572-4b2c-907d-281570a0f26b">DSSSEED</a> structure are not available, then the counter element of the structure should be 0xFFFFFFFF.


## -remarks



<b>DSSPUBKEY_VER3</b> is an alias for this structure.




## -see-also




<a href="https://msdn.microsoft.com/99d41222-b4ca-40f3-a240-52b0a9b3a9aa">BLOBHEADER</a>



<a href="https://msdn.microsoft.com/fbf2b5e4-b572-4b2c-907d-281570a0f26b">DSSSEED</a>
 

 

