---
UID: NC:mssip.pCryptSIPGetCaps
title: pCryptSIPGetCaps (mssip.h)
description: Is implemented by an subject interface package (SIP) to report capabilities.
helpviewer_keywords: ["mssip/pCryptSIPGetCaps","pCryptSIPGetCaps","pCryptSIPGetCaps callback","pCryptSIPGetCaps callback function [Security]","security.pfncryptsipgetcaps"]
old-location: security\pfncryptsipgetcaps.htm
tech.root: SecCrypto
ms.assetid: 8EA46B67-F542-4B15-81F4-3DD83DD45764
ms.date: 12/05/2018
ms.keywords: mssip/pCryptSIPGetCaps, pCryptSIPGetCaps, pCryptSIPGetCaps callback, pCryptSIPGetCaps callback function [Security], security.pfncryptsipgetcaps
f1_keywords:
- mssip/pCryptSIPGetCaps
dev_langs:
- c++
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- UserDefined
api_location:
- Mssip.h
api_name:
- pCryptSIPGetCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# pCryptSIPGetCaps callback function


## -description


The <b>pCryptSIPGetCaps</b> function is implemented by an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP) to report capabilities.


## -parameters




### -param *pSubjInfo [in]

Pointer to a [SIP_SUBJECTINFO](https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo) structure that specifies subject information data to the SIP APIs.


### -param *pCaps [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_cap_set_v2">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipgetcaps">CryptSIPGetCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_cap_set_v2">SIP_CAP_SET</a>



[SIP_SUBJECTINFO](https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo)
 

 

