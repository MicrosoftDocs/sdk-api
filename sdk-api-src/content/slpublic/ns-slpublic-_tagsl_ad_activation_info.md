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

# _tagSL_AD_ACTIVATION_INFO structure


## -description


Specifies information used for the retail or Active Directory phone activation of a license.


## -struct-fields




### -field header

 An <a href="https://msdn.microsoft.com/8209652d-c40e-419b-9929-647f03fed79c">SL_ACTIVATION_INFO_HEADER</a> structure that contains the activation type.  The activation type determines whether the <b>SL_AD_ACTIVATION_INFO</b> structure is used for retail or Active Directory phone activation.


### -field pwszProductKey

The product key.


### -field pwszActivationObjectName

The name of the activation object.


## -remarks



For an example of how this structure is used, see the description of the <i>pActivationInfo</i> parameter in the <a href="https://msdn.microsoft.com/14a2e84f-f5f7-4f17-8c7c-2cf580e14a26">SLActivateProduct</a>, <a href="https://msdn.microsoft.com/22817dc4-5d06-41bd-980d-b4402f74b82b">SLDepositOfflineConfirmationIdEx</a>, and <a href="https://msdn.microsoft.com/a9fd3717-7f1d-4f53-a246-c0542fc2e474">SLGenerateOfflineInstallationIdEx</a>  functions.




## -see-also




<a href="https://msdn.microsoft.com/14a2e84f-f5f7-4f17-8c7c-2cf580e14a26">SLActivateProduct</a>



<a href="https://msdn.microsoft.com/22817dc4-5d06-41bd-980d-b4402f74b82b">SLDepositOfflineConfirmationIdEx</a>



<a href="https://msdn.microsoft.com/a9fd3717-7f1d-4f53-a246-c0542fc2e474">SLGenerateOfflineInstallationIdEx</a>



<a href="https://msdn.microsoft.com/8209652d-c40e-419b-9929-647f03fed79c">SL_ACTIVATION_INFO_HEADER</a>



<a href="https://msdn.microsoft.com/e16a4e43-f7ef-43a3-a268-5f644340274c">SL_ACTIVATION_TYPE</a>
 

 

