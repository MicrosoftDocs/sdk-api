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

# _CRYPT_PROVIDER_REGDEFUSAGE structure


## -description


The <b>CRYPT_PROVIDER_REGDEFUSAGE</b> structure is used by the <a href="https://msdn.microsoft.com/511D05BD-0F8C-45B8-A1B0-D3C7AAFECCFC">WintrustAddDefaultForUsage</a> function to register callback information about a provider's default usage.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field pgActionID

GUID that specifies the provider's default action.


### -field pwszDllName

Pointer to the name of the provider DLL.


### -field pwszLoadCallbackDataFunctionName

Pointer to the name of the function that loads the callback data to be returned when the <a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a> function is called with the <i>dwAction</i> parameter set to <b>DWACTION_ALLOCANDFILL</b>. This information also exists in the <a href="https://msdn.microsoft.com/8fb68f44-6f69-4eac-90de-02689e3e86cf">WINTRUST_DATA</a> structure.


### -field pwszFreeCallbackDataFunctionName

Pointer to the name of the function that frees allocated memory when the <a href="https://msdn.microsoft.com/B2ED5489-792F-4B00-A21E-EE1B1462D1C8">WintrustGetDefaultForUsage</a> function is called with the <i>dwAction</i> parameter set to <b>DWACTION_FREE</b>. This information also exists in the <a href="https://msdn.microsoft.com/8fb68f44-6f69-4eac-90de-02689e3e86cf">WINTRUST_DATA</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/28A93F39-0CBC-432C-841B-83B54A50EA14">CRYPT_PROVIDER_DEFUSAGE</a>



<a href="https://msdn.microsoft.com/8fb68f44-6f69-4eac-90de-02689e3e86cf">WINTRUST_DATA</a>



<a href="https://msdn.microsoft.com/511D05BD-0F8C-45B8-A1B0-D3C7AAFECCFC">WintrustAddDefaultForUsage</a>
 

 

