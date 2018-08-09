---
UID: NF:wcmconfig.ITargetInfo.LoadModule
title: ITargetInfo::LoadModule
author: windows-sdk-content
description: Loads the module from the offline installation location.
old-location: smi\itargetinfo_loadmodule.htm
old-project: smi
ms.assetid: 863aefc6-d777-4af9-b310-adadef993bcd
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ITargetInfo interface [SMI],LoadModule method, ITargetInfo.LoadModule, ITargetInfo::LoadModule, LoadModule, LoadModule method [SMI], LoadModule method [SMI],ITargetInfo interface, smi.itargetinfo_loadmodule, wcmconfig/ITargetInfo::LoadModule
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
 - ITargetInfo.LoadModule
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ITargetInfo::LoadModule


## -description


Loads the module from the offline installation location.


## -parameters




### -param Module [in]

The name of the module.


### -param ModuleHandle [out]

The module handle.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

