---
UID: NS:slpublic._tagSL_AD_ACTIVATION_INFO
title: SL_AD_ACTIVATION_INFO
author: windows-sdk-content
description: Specifies information used for the retail or Active Directory phone activation of a license.
old-location: security\sl_ad_activation_info.htm
tech.root: SecSLApi
ms.assetid: 17012938-3E59-47DA-A046-8264CC3F06AF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSL_AD_ACTIVATION_INFO, PSL_AD_ACTIVATION_INFO structure pointer [Security], SL_AD_ACTIVATION_INFO, SL_AD_ACTIVATION_INFO structure [Security], security.sl_ad_activation_info, slpublic/PSL_AD_ACTIVATION_INFO, slpublic/SL_AD_ACTIVATION_INFO
ms.topic: struct
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - slpublic.h
api_name:
 - SL_AD_ACTIVATION_INFO
product: Windows
targetos: Windows
req.typenames: SL_AD_ACTIVATION_INFO
req.redist: 
---

# SL_AD_ACTIVATION_INFO structure


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
 

 

