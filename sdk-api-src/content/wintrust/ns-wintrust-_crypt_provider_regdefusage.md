---
UID: NS:wintrust._CRYPT_PROVIDER_REGDEFUSAGE
title: "_CRYPT_PROVIDER_REGDEFUSAGE"
author: windows-driver-content
description: Used by the WintrustAddDefaultForUsage function to register callback information about a provider's default usage.
old-location: security\crypt_provider_regdefusage.htm
old-project: SecCrypto
ms.assetid: A6047CBA-E4BA-4A31-B700-C368CFB57895
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCRYPT_PROVIDER_REGDEFUSAGE, CRYPT_PROVIDER_REGDEFUSAGE, CRYPT_PROVIDER_REGDEFUSAGE structure [Security], PCRYPT_PROVIDER_REGDEFUSAGE, PCRYPT_PROVIDER_REGDEFUSAGE structure pointer [Security], _CRYPT_PROVIDER_REGDEFUSAGE, security.crypt_provider_regdefusage, wintrust/CRYPT_PROVIDER_REGDEFUSAGE, wintrust/PCRYPT_PROVIDER_REGDEFUSAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPT_PROVIDER_REGDEFUSAGE, *PCRYPT_PROVIDER_REGDEFUSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wintrust.h
api_name:
-	CRYPT_PROVIDER_REGDEFUSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

