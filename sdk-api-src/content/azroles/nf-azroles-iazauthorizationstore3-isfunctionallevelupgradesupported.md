---
UID: NF:azroles.IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported
title: IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported (azroles.h)
description: Gets a Boolean value that indicates whether the version of this authorization store can be upgraded.
helpviewer_keywords: ["IAzAuthorizationStore3 interface [Security]","IsFunctionalLevelUpgradeSupported method","IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported","IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported","IsFunctionalLevelUpgradeSupported","IsFunctionalLevelUpgradeSupported method [Security]","IsFunctionalLevelUpgradeSupported method [Security]","IAzAuthorizationStore3 interface","azroles/IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported","security.iazauthorizationstore3_isfunctionallevelupgradesupported"]
old-location: security\iazauthorizationstore3_isfunctionallevelupgradesupported.htm
tech.root: security
ms.assetid: 344fbbb7-72e7-46ec-a924-79fece3e1eb0
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],IsFunctionalLevelUpgradeSupported method, IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported, IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported, IsFunctionalLevelUpgradeSupported, IsFunctionalLevelUpgradeSupported method [Security], IsFunctionalLevelUpgradeSupported method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported, security.iazauthorizationstore3_isfunctionallevelupgradesupported
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
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
 - IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported
 - azroles/IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported
---

# IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported


## -description

The <b>IsFunctionalLevelUpgradeSupported</b> method gets a Boolean  value that indicates whether the version of this authorization store can be upgraded.

## -parameters

### -param lFunctionalLevel [in]

The version to check. Set this parameter   to <b>AZ_AZSTORE_NT6_FUNCTION_LEVEL</b>.

### -param pbSupported [out]

<b>VARIANT_TRUE</b>  if the underlying authorization store supports version 2 functionality; otherwise, <b>VARIANT_FALSE</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore3">IAzAuthorizationStore3</a>



<a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-upgradestoresfunctionallevel">UpgradeStoresFunctionalLevel</a>