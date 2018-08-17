---
UID: NF:azroles.IAzAuthorizationStore3.UpgradeStoresFunctionalLevel
title: IAzAuthorizationStore3::UpgradeStoresFunctionalLevel
author: windows-sdk-content
description: Upgrades this authorization store from version 1 to version 2.
old-location: security\iazauthorizationstore3_upgradestoresfunctionallevel_method.htm
old-project: secauthz
ms.assetid: 7719e3fd-5b06-468c-9034-f1f0bb41a5be
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],UpgradeStoresFunctionalLevel method, IAzAuthorizationStore3.UpgradeStoresFunctionalLevel, IAzAuthorizationStore3::UpgradeStoresFunctionalLevel, UpgradeStoresFunctionalLevel, UpgradeStoresFunctionalLevel method [Security], UpgradeStoresFunctionalLevel method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::UpgradeStoresFunctionalLevel, security.iazauthorizationstore3_upgradestoresfunctionallevel_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzAuthorizationStore3.UpgradeStoresFunctionalLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzAuthorizationStore3::UpgradeStoresFunctionalLevel


## -description


The <b>UpgradeStoresFunctionalLevel</b> method  upgrades this authorization store from version 1 to version 2. 


## -parameters




### -param lFunctionalLevel [in]

Specifies the version to which to upgrade the authorization store. Set the value of this parameter to  <b>AZ_AZSTORE_NT6_FUNCTION_LEVEL</b>


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If the authorization store being updated is an Active Directory store, this method checks whether the LDAP schema of the Active Directory store is updated. If the LDAP schema of the Active Directory store is not updated, the authorization store is not updated.



