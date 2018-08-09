---
UID: NF:wcmconfig.ISettingsEngine.CreateTargetInfo
title: ISettingsEngine::CreateTargetInfo
author: windows-sdk-content
description: Creates an empty target.
old-location: smi\isettingsengine_createtargetinfo.htm
old-project: smi
ms.assetid: f3d31643-c606-4fc1-96a8-cf5cb26bcf3f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateTargetInfo, CreateTargetInfo method [SMI], CreateTargetInfo method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],CreateTargetInfo method, ISettingsEngine.CreateTargetInfo, ISettingsEngine::CreateTargetInfo, smi.isettingsengine_createtargetinfo, wcmconfig/ISettingsEngine::CreateTargetInfo
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
 - ISettingsEngine.CreateTargetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsEngine::CreateTargetInfo


## -description


Creates an empty target.


## -parameters




### -param Target [out]

An <a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a> interface pointer to an empty target.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to create an ITargetInfo object.




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

