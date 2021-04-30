---
UID: NF:azroles.IAzAuthorizationStore3.UpgradeStoresFunctionalLevel
title: IAzAuthorizationStore3::UpgradeStoresFunctionalLevel (azroles.h)
description: Upgrades this authorization store from version 1 to version 2.
helpviewer_keywords: ["IAzAuthorizationStore3 interface [Security]","UpgradeStoresFunctionalLevel method","IAzAuthorizationStore3.UpgradeStoresFunctionalLevel","IAzAuthorizationStore3::UpgradeStoresFunctionalLevel","UpgradeStoresFunctionalLevel","UpgradeStoresFunctionalLevel method [Security]","UpgradeStoresFunctionalLevel method [Security]","IAzAuthorizationStore3 interface","azroles/IAzAuthorizationStore3::UpgradeStoresFunctionalLevel","security.iazauthorizationstore3_upgradestoresfunctionallevel_method"]
old-location: security\iazauthorizationstore3_upgradestoresfunctionallevel_method.htm
tech.root: security
ms.assetid: 7719e3fd-5b06-468c-9034-f1f0bb41a5be
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],UpgradeStoresFunctionalLevel method, IAzAuthorizationStore3.UpgradeStoresFunctionalLevel, IAzAuthorizationStore3::UpgradeStoresFunctionalLevel, UpgradeStoresFunctionalLevel, UpgradeStoresFunctionalLevel method [Security], UpgradeStoresFunctionalLevel method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::UpgradeStoresFunctionalLevel, security.iazauthorizationstore3_upgradestoresfunctionallevel_method
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
 - IAzAuthorizationStore3::UpgradeStoresFunctionalLevel
 - azroles/IAzAuthorizationStore3::UpgradeStoresFunctionalLevel
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
 - IAzAuthorizationStore3.UpgradeStoresFunctionalLevel
---

# IAzAuthorizationStore3::UpgradeStoresFunctionalLevel


## -description

The <b>UpgradeStoresFunctionalLevel</b> method  upgrades this authorization store from version 1 to version 2.

## -parameters

### -param lFunctionalLevel [in]

Specifies the version to which to upgrade the authorization store. Set the value of this parameter to  <b>AZ_AZSTORE_NT6_FUNCTION_LEVEL</b>

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If the authorization store being updated is an Active Directory store, this method checks whether the LDAP schema of the Active Directory store is updated. If the LDAP schema of the Active Directory store is not updated, the authorization store is not updated.