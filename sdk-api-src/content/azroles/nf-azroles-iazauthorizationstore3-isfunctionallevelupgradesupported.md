---
UID: NF:azroles.IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported
title: IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported
author: windows-sdk-content
description: Gets a Boolean value that indicates whether the version of this authorization store can be upgraded.
old-location: security\iazauthorizationstore3_isfunctionallevelupgradesupported.htm
old-project: SecAuthZ
ms.assetid: 344fbbb7-72e7-46ec-a924-79fece3e1eb0
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IAzAuthorizationStore3 interface [Security],IsFunctionalLevelUpgradeSupported method, IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported, IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported, IsFunctionalLevelUpgradeSupported, IsFunctionalLevelUpgradeSupported method [Security], IsFunctionalLevelUpgradeSupported method [Security],IAzAuthorizationStore3 interface, azroles/IAzAuthorizationStore3::IsFunctionalLevelUpgradeSupported, security.iazauthorizationstore3_isfunctionallevelupgradesupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.h
api_name:
-	IAzAuthorizationStore3.IsFunctionalLevelUpgradeSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/7063416c-b132-4b3a-bb2b-d27fccea25e4">IAzAuthorizationStore3</a>



<a href="https://msdn.microsoft.com/7719e3fd-5b06-468c-9034-f1f0bb41a5be">UpgradeStoresFunctionalLevel</a>
 

 

