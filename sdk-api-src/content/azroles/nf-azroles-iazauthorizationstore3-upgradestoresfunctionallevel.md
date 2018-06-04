---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



