---
UID: NF:wcmconfig.ISettingsEngine.CreateSettingsContext
title: ISettingsEngine::CreateSettingsContext
author: windows-sdk-content
description: Creates a settings context.
old-location: smi\isettingsengine_createsettingscontext.htm
old-project: smi
ms.assetid: a9fe2c24-f696-4726-8e67-07280c8e8a3e
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateSettingsContext, CreateSettingsContext method [SMI], CreateSettingsContext method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],CreateSettingsContext method, ISettingsEngine.CreateSettingsContext, ISettingsEngine::CreateSettingsContext, smi.isettingsengine_createsettingscontext, wcmconfig/ISettingsEngine::CreateSettingsContext
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
 - ISettingsEngine.CreateSettingsContext
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsEngine::CreateSettingsContext


## -description


Creates a settings context.


## -parameters




### -param Flags [in]

The value of the Flags parameter may be 0, indicating "normal mode"  or 0x00000001, indicating <b>LIMITED_VALIDATION_MODE</b>. In normal mode, the settings context validates any changes made to list items against the current state of the target image. For example, if an  attempt is made to create a list element that already exists in the image, the create operation fails. In <b>LIMITED_VALIDATION_MODE</b>, contradictory data is not accepted. You cannot modify and then add a list item. However, no attempt is made to verify the changes made against the current state of the system. Only use <b>LIMITED_VALIDATION_MODE</b> when the intention is to author a context which is to be serialized. Do not specify this flag when creating a context to be used for <a href="https://msdn.microsoft.com/459a97fb-e5fb-42a5-998d-84631fec2e6f">ISettingsEngine::ApplySettingsContext</a>. If used, the context may not be sufficiently validated and may fail during an application.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param SettingsContext [out]

A pointer to an <a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a> object that represents the created context.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there were insufficient resources to create the <a href="https://msdn.microsoft.com/29f43c3f-57bf-4208-a0bf-9b4414795a59">ISettingsContext</a> object.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

