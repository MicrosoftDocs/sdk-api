---
UID: NS:wincrypt._CERT_DH_PARAMETERS
title: "_CERT_DH_PARAMETERS"
author: windows-sdk-content
description: Contains parameters associated with a Diffie/Hellman public key algorithm.
old-location: security\cert_dh_parameters.htm
tech.root: seccrypto
ms.assetid: bd57236a-1763-4a43-83f4-95131d8adec9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCERT_DH_PARAMETERS, CERT_DH_PARAMETERS, CERT_DH_PARAMETERS structure [Security], PCERT_DH_PARAMETERS, PCERT_DH_PARAMETERS structure pointer [Security], _CERT_DH_PARAMETERS, _crypto2_cert_dh_parameters, security.cert_dh_parameters, wincrypt/CERT_DH_PARAMETERS, wincrypt/PCERT_DH_PARAMETERS"
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
 - CERT_DH_PARAMETERS
product: Windows
targetos: Windows
req.typenames: CERT_DH_PARAMETERS, *PCERT_DH_PARAMETERS
req.redist: 
---

# _CERT_DH_PARAMETERS structure


## -description


The <b>CERT_DH_PARAMETERS</b> structure contains parameters associated with a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie/Hellman</a> public key algorithm.


## -struct-fields




### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.


### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).

