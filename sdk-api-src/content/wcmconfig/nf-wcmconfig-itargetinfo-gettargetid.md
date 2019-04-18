---
UID: NF:wcmconfig.ITargetInfo.GetTargetID
title: ITargetInfo::GetTargetID (wcmconfig.h)
author: windows-sdk-content
description: Gets the unique identifier associated with the current target.
old-location: smi\itargetinfo_gettargetid.htm
tech.root: SMI
ms.assetid: b80e3363-8efa-44b7-a61e-66177d1c53ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTargetID, GetTargetID method [SMI], GetTargetID method [SMI],ITargetInfo interface, ITargetInfo interface [SMI],GetTargetID method, ITargetInfo.GetTargetID, ITargetInfo::GetTargetID, smi.itargetinfo_gettargetid, wcmconfig/ITargetInfo::GetTargetID
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
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo.GetTargetID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITargetInfo::GetTargetID


## -description


Gets the unique identifier associated with the current target.


## -parameters




### -param TargetID [out]

The unique identifier associated with the current target.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.




## -see-also




<a href="https://msdn.microsoft.com/f1dd3c93-43ca-4804-8330-55acaccf8ea8">ITargetInfo</a>
 

 

