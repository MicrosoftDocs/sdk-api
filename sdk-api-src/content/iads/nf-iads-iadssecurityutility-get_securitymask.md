---
UID: NF:iads.IADsSecurityUtility.get_SecurityMask
title: IADsSecurityUtility::get_SecurityMask (iads.h)
description: Determines which elements of the security descriptor to retrieve or set. (Get)
helpviewer_keywords: ["IADsSecurityUtility interface [ADSI]","SecurityMask property","IADsSecurityUtility.SecurityMask","IADsSecurityUtility.get_SecurityMask","IADsSecurityUtility::SecurityMask","IADsSecurityUtility::get_SecurityMask","IADsSecurityUtility::put_SecurityMask","SecurityMask property [ADSI]","SecurityMask property [ADSI]","IADsSecurityUtility interface","adsi.iadssecurityutility_securitymask","get_SecurityMask","iads/IADsSecurityUtility::SecurityMask","iads/IADsSecurityUtility::get_SecurityMask","iads/IADsSecurityUtility::put_SecurityMask"]
old-location: adsi\iadssecurityutility_securitymask.htm
tech.root: adsi
ms.assetid: b54ebe68-f7ce-484e-9378-04662b7a1051
ms.date: 12/05/2018
ms.keywords: IADsSecurityUtility interface [ADSI],SecurityMask property, IADsSecurityUtility.SecurityMask, IADsSecurityUtility.get_SecurityMask, IADsSecurityUtility::SecurityMask, IADsSecurityUtility::get_SecurityMask, IADsSecurityUtility::put_SecurityMask, SecurityMask property [ADSI], SecurityMask property [ADSI],IADsSecurityUtility interface, adsi.iadssecurityutility_securitymask, get_SecurityMask, iads/IADsSecurityUtility::SecurityMask, iads/IADsSecurityUtility::get_SecurityMask, iads/IADsSecurityUtility::put_SecurityMask
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsSecurityUtility::get_SecurityMask
 - iads/IADsSecurityUtility::get_SecurityMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility.SecurityMask
 - IADsSecurityUtility.get_SecurityMask
 - IADsSecurityUtility.put_SecurityMask
---

# IADsSecurityUtility::get_SecurityMask


## -description

The <b>SecurityMask</b> property determines which elements of the security descriptor to retrieve or set. This property must be set prior to calling <a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor">IADsSecurityUtility.GetSecurityDescriptor</a> or <a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor">IADsSecurityUtility.SetSecurityDescriptor</a>.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_security_info_enum">ADS_SECURITY_INFO_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>



<a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor">IADsSecurityUtility.GetSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor">IADsSecurityUtility.SetSecurityDescriptor</a>
