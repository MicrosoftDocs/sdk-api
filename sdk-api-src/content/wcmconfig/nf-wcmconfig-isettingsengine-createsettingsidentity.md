---
UID: NF:wcmconfig.ISettingsEngine.CreateSettingsIdentity
title: ISettingsEngine::CreateSettingsIdentity method
author: windows-driver-content
description: Creates an empty settings identity.
old-location: smi\isettingsengine_createsettingsidentity.htm
old-project: SMI
ms.assetid: b48e6784-5565-4809-873e-cadedce57743
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateSettingsIdentity method [SMI], CreateSettingsIdentity method [SMI], ISettingsEngine interface, CreateSettingsIdentity,ISettingsEngine.CreateSettingsIdentity, ISettingsEngine, ISettingsEngine interface [SMI], CreateSettingsIdentity method, ISettingsEngine::CreateSettingsIdentity, smi.isettingsengine_createsettingsidentity, wcmconfig/ISettingsEngine::CreateSettingsIdentity
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
-	ISettingsEngine.CreateSettingsIdentity
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsEngine::CreateSettingsIdentity method


## -description


Creates an empty settings identity.


## -parameters




### -param SettingsID [out]

A value that returns a pointer to an empty <a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsIdentity</a> object.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to allocate the <a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsIdentity</a> object.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

