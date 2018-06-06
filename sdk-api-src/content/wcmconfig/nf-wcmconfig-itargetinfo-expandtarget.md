---
UID: NF:wcmconfig.ITargetInfo.ExpandTarget
title: ITargetInfo::ExpandTarget
author: windows-sdk-content
description: Expands a location string to indicate the offline installation location.
old-location: smi\itargetinfo_expandtarget.htm
old-project: SMI
ms.assetid: c9c757f4-ad71-42d7-864a-26f3d1e8000b
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ExpandTarget, ExpandTarget method [SMI], ExpandTarget method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],ExpandTarget method, ITargetInfo.ExpandTarget, ITargetInfo::ExpandTarget, smi.itargetinfo_expandtarget, wcmconfig/ITargetInfo::ExpandTarget
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
 - ITargetInfo.ExpandTarget
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ITargetInfo::ExpandTarget


## -description


Expands a location string to indicate the offline installation location.


## -parameters




### -param Offline [in]

<b>True</b> if the installation location is offline.


### -param Location [in]

The location string.


### -param ExpandedLocation [out]

The expanded location string.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. This method may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.




## -see-also




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

