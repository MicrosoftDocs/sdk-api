---
UID: NF:mssip.CryptSIPGetCaps
title: CryptSIPGetCaps function (mssip.h)
author: windows-sdk-content
description: Retrieves the capabilities of a subject interface package (SIP).
old-location: security\cryptsipgetcaps.htm
tech.root: SecCrypto
ms.assetid: F939F6D5-DDFE-478F-8FDD-8FA9FAB26010
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptSIPGetCaps, CryptSIPGetCaps function [Security], mssip/CryptSIPGetCaps, security.cryptsipgetcaps
ms.topic: function
f1_keywords:
- mssip/CryptSIPGetCaps
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CryptSIPGetCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptSIPGetCaps function


## -description


The <b>CryptSIPGetCaps</b> function retrieves the capabilities of a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP).


## -parameters




### -param pSubjInfo [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a> structure that specifies subject information data to the SIP APIs.


### -param pCaps [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_cap_set_v2">SIP_CAP_SET</a> structure that defines the capabilities of an SIP.


## -remarks



Unlike other SIP functions, <b>CryptSIPGetCaps</b> is not registered in the dispatch table. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_dispatch_info_">SIP_DISPATCH_INFO</a> structure. Instead, callers must map the object identifier (OID) to the function entry point. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_cap_set_v2">SIP_CAP_SET</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_subjectinfo_">SIP_SUBJECTINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nc-mssip-pcryptsipgetcaps">pCryptSIPGetCaps</a>
 

 

