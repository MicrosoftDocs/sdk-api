---
UID: NF:wcmconfig.ISettingsResult.GetDescription
title: ISettingsResult::GetDescription
author: windows-sdk-content
description: Returns the description of the error.
old-location: smi\isettingsresult_getdescription.htm
old-project: SMI
ms.assetid: d020bd46-8967-4105-856d-ee448b527852
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetDescription, GetDescription method [SMI], GetDescription method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetDescription method, ISettingsResult.GetDescription, ISettingsResult::GetDescription, smi.isettingsresult_getdescription, wcmconfig/ISettingsResult::GetDescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsResult.GetDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsResult::GetDescription


## -description


Returns the description of the error.


## -parameters




### -param description [out]

The text that describes the error.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.




## -see-also




<a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a>
 

 

