---
UID: NF:wcmconfig.ISettingsIdentity.SetAttribute
title: ISettingsIdentity::SetAttribute method
author: windows-driver-content
description: Sets an identity attribute for a namespace identity.
old-location: smi\isettingsidentity_setattribute.htm
old-project: SMI
ms.assetid: 498bb364-3da8-456d-8e77-22b508516de0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISettingsIdentity, ISettingsIdentity interface [SMI], SetAttribute method, ISettingsIdentity::SetAttribute, SetAttribute method [SMI], SetAttribute method [SMI], ISettingsIdentity interface, SetAttribute,ISettingsIdentity.SetAttribute, smi.isettingsidentity_setattribute, wcmconfig/ISettingsIdentity::SetAttribute
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
-	ISettingsIdentity.SetAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsIdentity::SetAttribute method


## -description


Sets an identity attribute for a namespace identity.


## -parameters




### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param Name [in]

The name of the attribute.


### -param Value [in]

The value of the attribute.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It returns <b>WCM_E_ATTRIBUTENOTALLOWED</b> if the attribute specified by Name is not recognized.




## -see-also




<a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a>
 

 

