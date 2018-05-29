---
UID: NF:wcmconfig.ISettingsResult.GetContextDescription
title: ISettingsResult::GetContextDescription
author: windows-sdk-content
description: Returns the description of the context that surrounds the error.
old-location: smi\isettingsresult_getcontextdescription.htm
old-project: SMI
ms.assetid: d2bb39ce-9c49-46ab-b7d7-e4e4794f6b5a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetContextDescription, GetContextDescription method [SMI], GetContextDescription method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetContextDescription method, ISettingsResult.GetContextDescription, ISettingsResult::GetContextDescription, smi.isettingsresult_getcontextdescription, wcmconfig/ISettingsResult::GetContextDescription
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
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsResult.GetContextDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsResult::GetContextDescription


## -description


Returns the description of the context that surrounds the error.


## -parameters




### -param description [out]

The text that describes the context.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.




## -see-also




<a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a>
 

 

