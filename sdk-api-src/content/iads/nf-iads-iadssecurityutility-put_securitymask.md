---
UID: NF:iads.IADsSecurityUtility.put_SecurityMask
title: IADsSecurityUtility::put_SecurityMask (iads.h)
description: Determines which elements of the security descriptor to retrieve or set. (Put)
helpviewer_keywords: ["IADsSecurityUtility interface [ADSI]","SecurityMask property","IADsSecurityUtility.SecurityMask","IADsSecurityUtility.put_SecurityMask","IADsSecurityUtility::SecurityMask","IADsSecurityUtility::get_SecurityMask","IADsSecurityUtility::put_SecurityMask","SecurityMask property [ADSI]","SecurityMask property [ADSI]","IADsSecurityUtility interface","adsi.iadssecurityutility_securitymask","iads/IADsSecurityUtility::SecurityMask","iads/IADsSecurityUtility::get_SecurityMask","iads/IADsSecurityUtility::put_SecurityMask","put_SecurityMask"]
old-location: adsi\iadssecurityutility_securitymask.htm
tech.root: adsi
ms.assetid: b54ebe68-f7ce-484e-9378-04662b7a1051
ms.date: 02/14/2023
ms.keywords: IADsSecurityUtility interface [ADSI],SecurityMask property, IADsSecurityUtility.SecurityMask, IADsSecurityUtility.put_SecurityMask, IADsSecurityUtility::SecurityMask, IADsSecurityUtility::get_SecurityMask, IADsSecurityUtility::put_SecurityMask, SecurityMask property [ADSI], SecurityMask property [ADSI],IADsSecurityUtility interface, adsi.iadssecurityutility_securitymask, iads/IADsSecurityUtility::SecurityMask, iads/IADsSecurityUtility::get_SecurityMask, iads/IADsSecurityUtility::put_SecurityMask, put_SecurityMask
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
 - IADsSecurityUtility::put_SecurityMask
 - iads/IADsSecurityUtility::put_SecurityMask
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

# IADsSecurityUtility::put_SecurityMask

## -description

The **SecurityMask** property determines which elements of the security descriptor to retrieve or set. This property must be set prior to calling [IADsSecurityUtility.GetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor) or [IADsSecurityUtility.SetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor).

This property is read/write.

## -parameters

### -param lnSecurityMask

Specifies the security information to retrieve or set.

## -returns

An **HRESULT** value that indicates the success or failure of the call.

## -see-also

[ADS_SECURITY_INFO_ENUM](/windows/win32/api/iads/ne-iads-ads_security_info_enum)

[IADsSecurityUtility](/windows/win32/api/iads/nn-iads-iadssecurityutility)

[IADsSecurityUtility.GetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor)

[IADsSecurityUtility.SetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor)
