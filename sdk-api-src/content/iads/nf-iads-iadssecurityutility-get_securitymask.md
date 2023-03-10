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

The **SecurityMask** property determines which elements of the security descriptor to retrieve or set. This property must be set prior to calling [IADsSecurityUtility.GetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor) or [IADsSecurityUtility.SetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor).

This property is read/write.

## -parameters

### -param retval

`[out]` A pointer to a variable that receives the security mask.

## -returns

An **HRESULT** value that indicates the success or failure of the call.

## -see-also

[ADS_SECURITY_INFO_ENUM](/windows/win32/api/iads/ne-iads-ads_security_info_enum)

[IADsSecurityUtility](/windows/win32/api/iads/nn-iads-iadssecurityutility)

[IADsSecurityUtility.GetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-getsecuritydescriptor)

[IADsSecurityUtility.SetSecurityDescriptor](/windows/win32/api/iads/nf-iads-iadssecurityutility-setsecuritydescriptor)
