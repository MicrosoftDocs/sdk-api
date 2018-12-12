---
UID: NS:wincrypt._CERT_DSS_PARAMETERS
title: CERT_DSS_PARAMETERS
author: windows-sdk-content
description: Contains parameters associated with a Digital Signature Standard (DSS) public key algorithm.
old-location: security\cert_dss_parameters.htm
tech.root: seccrypto
ms.assetid: 4544986a-8168-4d56-be5f-59d318da7c30
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_DSS_PARAMETERS, CERT_DSS_PARAMETERS, CERT_DSS_PARAMETERS structure [Security], PCERT_DSS_PARAMETERS, PCERT_DSS_PARAMETERS structure pointer [Security], _crypto2_cert_dss_parameters, security.cert_dss_parameters, wincrypt/CERT_DSS_PARAMETERS, wincrypt/PCERT_DSS_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CERT_DSS_PARAMETERS
product: Windows
targetos: Windows
req.typenames: CERT_DSS_PARAMETERS, *PCERT_DSS_PARAMETERS
req.redist: 
---

# CERT_DSS_PARAMETERS structure


## -description


The <b>CERT_DSS_PARAMETERS</b> structure contains parameters associated with a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Standard</a> (DSS) <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> algorithm.


## -struct-fields




### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.


### -field q

Prime Q. It is 20 bytes in length. The most significant bit of the most significant byte must be set to 1.


### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).

