---
UID: NF:wcmconfig.ISettingsIdentity.GetAttribute
title: ISettingsIdentity::GetAttribute method
author: windows-driver-content
description: Gets an identity attribute for a namespace identity.
old-location: smi\isettingsidentity_getattribute.htm
old-project: SMI
ms.assetid: d79bf4be-f3ed-426b-a880-b9ab8aee0092
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAttribute method [SMI], GetAttribute method [SMI], ISettingsIdentity interface, GetAttribute,ISettingsIdentity.GetAttribute, ISettingsIdentity, ISettingsIdentity interface [SMI], GetAttribute method, ISettingsIdentity::GetAttribute, smi.isettingsidentity_getattribute, wcmconfig/ISettingsIdentity::GetAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ISettingsIdentity.GetAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsIdentity::GetAttribute method


## -description


Gets an identity attribute for a namespace identity.


## -parameters




### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param Name [in]

The name of the attribute.


### -param Value [out]

The value of the attribute.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. If the attribute specified by Name is not recognized, this function returns <b>WCM_E_ATTRIBUTENOTFOUND</b>.




## -see-also




<a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a>
 

 

