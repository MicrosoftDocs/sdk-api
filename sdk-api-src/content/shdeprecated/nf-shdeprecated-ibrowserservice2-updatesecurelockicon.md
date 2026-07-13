---
UID: NF:shdeprecated.IBrowserService2.UpdateSecureLockIcon
title: IBrowserService2::UpdateSecureLockIcon (shdeprecated.h)
description: Deprecated. Updates the value of the _eSecureLockIcon member of the BASEBROWSERDATA structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","UpdateSecureLockIcon method","IBrowserService2.UpdateSecureLockIcon","IBrowserService2::UpdateSecureLockIcon","SECURELOCK_FIRSTSUGGEST","SECURELOCK_NOCHANGE","SECURELOCK_SET_FORTEZZA","SECURELOCK_SET_MIXED","SECURELOCK_SET_SECURE128BIT","SECURELOCK_SET_SECURE40BIT","SECURELOCK_SET_SECURE56BIT","SECURELOCK_SET_SECUREUNKNOWNBIT","SECURELOCK_SET_UNSECURE","SECURELOCK_SUGGEST_FORTEZZA","SECURELOCK_SUGGEST_MIXED","SECURELOCK_SUGGEST_SECURE128BIT","SECURELOCK_SUGGEST_SECURE40BIT","SECURELOCK_SUGGEST_SECURE56BIT","SECURELOCK_SUGGEST_SECUREUNKNOWNBIT","SECURELOCK_SUGGEST_UNSECURE","UpdateSecureLockIcon","UpdateSecureLockIcon method [Windows Shell]","UpdateSecureLockIcon method [Windows Shell]","IBrowserService2 interface","shdeprecated/IBrowserService2::UpdateSecureLockIcon","shell.IBrowserService2_UpdateSecureLockIcon","zone_IBrowserService2_UpdateSecureLockIcon"]
old-location: shell\IBrowserService2_UpdateSecureLockIcon.htm
tech.root: shell
ms.assetid: 4a24244d-197e-4df4-bcd9-546c999b2534
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],UpdateSecureLockIcon method, IBrowserService2.UpdateSecureLockIcon, IBrowserService2::UpdateSecureLockIcon, SECURELOCK_FIRSTSUGGEST, SECURELOCK_NOCHANGE, SECURELOCK_SET_FORTEZZA, SECURELOCK_SET_MIXED, SECURELOCK_SET_SECURE128BIT, SECURELOCK_SET_SECURE40BIT, SECURELOCK_SET_SECURE56BIT, SECURELOCK_SET_SECUREUNKNOWNBIT, SECURELOCK_SET_UNSECURE, SECURELOCK_SUGGEST_FORTEZZA, SECURELOCK_SUGGEST_MIXED, SECURELOCK_SUGGEST_SECURE128BIT, SECURELOCK_SUGGEST_SECURE40BIT, SECURELOCK_SUGGEST_SECURE56BIT, SECURELOCK_SUGGEST_SECUREUNKNOWNBIT, SECURELOCK_SUGGEST_UNSECURE, UpdateSecureLockIcon, UpdateSecureLockIcon method [Windows Shell], UpdateSecureLockIcon method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::UpdateSecureLockIcon, shell.IBrowserService2_UpdateSecureLockIcon, zone_IBrowserService2_UpdateSecureLockIcon
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::UpdateSecureLockIcon
 - shdeprecated/IBrowserService2::UpdateSecureLockIcon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.UpdateSecureLockIcon
---

# IBrowserService2::UpdateSecureLockIcon


## -description

Deprecated. Updates the value of the <b>_eSecureLockIcon</b> member of the <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a> structure, which tracks the icon indicating a secure site, as well as updating the icon itself in the UI.

## -parameters

### -param eSecureLock [in]

Type: <b>int</b>

One of the following values indicating the secure lock status. Note that each value is provided in a SET and SUGGEST form. For more details, see <a href="/windows/desktop/api/shdeprecated/ns-shdeprecated-basebrowserdatalh">BASEBROWSERDATA</a>.





#### SECURELOCK_NOCHANGE



#### SECURELOCK_SET_UNSECURE



#### SECURELOCK_SET_MIXED



#### SECURELOCK_SET_SECUREUNKNOWNBIT



#### SECURELOCK_SET_SECURE40BIT



#### SECURELOCK_SET_SECURE56BIT



#### SECURELOCK_SET_FORTEZZA



#### SECURELOCK_SET_SECURE128BIT



#### SECURELOCK_FIRSTSUGGEST



#### SECURELOCK_SUGGEST_UNSECURE



#### SECURELOCK_SUGGEST_MIXED



#### SECURELOCK_SUGGEST_SECUREUNKNOWNBIT



#### SECURELOCK_SUGGEST_SECURE40BIT



#### SECURELOCK_SUGGEST_SECURE56BIT



#### SECURELOCK_SUGGEST_FORTEZZA



#### SECURELOCK_SUGGEST_SECURE128BIT

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

SECURELOCK_SUGGEST_UNSECURE is equivalent to SECURELOCK_FIRSTSUGGEST.