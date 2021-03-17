---
UID: NF:imapi2.IBurnVerification.get_BurnVerificationLevel
title: IBurnVerification::get_BurnVerificationLevel (imapi2.h)
description: Retrieves the current Burn Verification Level.
helpviewer_keywords: ["IBurnVerification interface [IMAPI]","get_BurnVerificationLevel method","IBurnVerification.get_BurnVerificationLevel","IBurnVerification::get_BurnVerificationLevel","get_BurnVerificationLevel","get_BurnVerificationLevel method [IMAPI]","get_BurnVerificationLevel method [IMAPI]","IBurnVerification interface","imapi.iburnverification_get_burnverificationlevel","imapi2/IBurnVerification::get_BurnVerificationLevel"]
old-location: imapi\iburnverification_get_burnverificationlevel.htm
tech.root: imapi
ms.assetid: 4be9191a-8f87-4571-a7b6-60d582ec471d
ms.date: 12/05/2018
ms.keywords: IBurnVerification interface [IMAPI],get_BurnVerificationLevel method, IBurnVerification.get_BurnVerificationLevel, IBurnVerification::get_BurnVerificationLevel, get_BurnVerificationLevel, get_BurnVerificationLevel method [IMAPI], get_BurnVerificationLevel method [IMAPI],IBurnVerification interface, imapi.iburnverification_get_burnverificationlevel, imapi2/IBurnVerification::get_BurnVerificationLevel
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBurnVerification::get_BurnVerificationLevel
 - imapi2/IBurnVerification::get_BurnVerificationLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IBurnVerification.get_BurnVerificationLevel
---

# IBurnVerification::get_BurnVerificationLevel


## -description

Retrieves  the current Burn Verification Level.

## -parameters

### -param value

Pointer to an <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_burn_verification_level">IMAPI_BURN_VERIFICATION_LEVEL</a> enumeration that specifies the current the Burn Verification Level.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification">IBurnVerification</a>



<a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_burn_verification_level">IMAPI_BURN_VERIFICATION_LEVEL</a>