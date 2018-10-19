---
UID: NS:wincrypt._CERT_PAIR
title: "_CERT_PAIR"
author: windows-sdk-content
description: The CERT_PAIR structure contains a certificate and its pair cross certificate.
old-location: security\cert_pair.htm
tech.root: seccrypto
ms.assetid: b5929430-1b12-4ebf-a5ef-3669bba63f8c
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PCERT_PAIR, CERT_PAIR, CERT_PAIR structure [Security], PCERT_PAIR, PCERT_PAIR structure pointer [Security], _CERT_PAIR, _crypto2_cert_pair, security.cert_pair, wincrypt/CERT_PAIR, wincrypt/PCERT_PAIR"
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
 - CERT_PAIR
product: Windows
targetos: Windows
req.typenames: CERT_PAIR, *PCERT_PAIR
req.redist: 
---

# _CERT_PAIR structure


## -description


The <b>CERT_PAIR</b> structure contains a certificate and its pair cross certificate.


## -struct-fields




### -field Forward

An optional <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a> structure that contains a certificate. If the <b>cbData</b> member of <b>Forward</b> is zero, the certificate may be empty.


### -field Reverse

An optional <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a> structure that contains a certificate. If the <b>cbData</b> member of <b>Reverse</b> is zero, the certificate may be empty.

