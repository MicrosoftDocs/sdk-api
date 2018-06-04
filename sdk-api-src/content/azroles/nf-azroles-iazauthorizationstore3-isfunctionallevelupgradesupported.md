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
 

 

