---
UID: NS:wincrypt._CERT_GENERAL_SUBTREE
title: "_CERT_GENERAL_SUBTREE"
author: windows-sdk-content
description: The CERT_GENERAL_SUBTREE structure is used in CERT_NAME_CONSTRAINTS_INFO structure. This structure provides the identity of a certificate that can be included or excluded.
old-location: security\cert_general_subtree.htm
old-project: seccrypto
ms.assetid: 991e277c-46f5-4987-ab48-0d1c1442273f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCERT_GENERAL_SUBTREE, CERT_GENERAL_SUBTREE, CERT_GENERAL_SUBTREE structure [Security], PCERT_GENERAL_SUBTREE, PCERT_GENERAL_SUBTREE structure pointer [Security], _CERT_GENERAL_SUBTREE, _crypto2_cert_general_subtree, security.cert_general_subtree, wincrypt/CERT_GENERAL_SUBTREE, wincrypt/PCERT_GENERAL_SUBTREE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CERT_GENERAL_SUBTREE, *PCERT_GENERAL_SUBTREE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_GENERAL_SUBTREE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_GENERAL_SUBTREE structure


## -description


The <b>CERT_GENERAL_SUBTREE</b> structure is used in 
<a href="https://msdn.microsoft.com/16a57c4b-905f-40c0-b298-71f0534bfa5a">CERT_NAME_CONSTRAINTS_INFO</a> structure. This structure provides the identity of a certificate that can be included or excluded.


## -struct-fields




### -field Base


<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a> containing a base name identifier of a certificate.


### -field dwMinimum

Currently not used.


### -field fMaximum

Currently not used.


### -field dwMaximum

Currently not used.

