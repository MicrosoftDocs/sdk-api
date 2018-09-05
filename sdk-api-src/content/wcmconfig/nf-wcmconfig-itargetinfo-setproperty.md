---
UID: NF:wcmconfig.ITargetInfo.SetProperty
title: ITargetInfo::SetProperty
author: windows-sdk-content
description: Sets a property value for the offline installation location.
old-location: smi\itargetinfo_setproperty.htm
old-project: SMI
ms.assetid: ecd93710-a9e8-41cf-b30c-97d1efe0fa6f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITargetInfo interface [SMI],SetProperty method, ITargetInfo.SetProperty, ITargetInfo::SetProperty, SetProperty, SetProperty method [SMI], SetProperty method [SMI],ITargetInfo interface, smi.itargetinfo_setproperty, wcmconfig/ITargetInfo::SetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.redist: 
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
 - ITargetInfo.SetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ITargetInfo::SetProperty


## -description


Sets a property value for the offline installation location.


## -parameters




### -param Offline [in]

<b>True</b> if installation location is offline.


### -param Property [in]

The name of the property.


### -param Value [in]

The value of the property.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success.




## -see-also




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

