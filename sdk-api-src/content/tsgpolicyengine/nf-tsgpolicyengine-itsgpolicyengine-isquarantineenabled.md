---
UID: NF:tsgpolicyengine.ITSGPolicyEngine.IsQuarantineEnabled
title: ITSGPolicyEngine::IsQuarantineEnabled
author: windows-sdk-content
description: Indicates whether the authorization plug-in requires a statement of health (SoH) from the user's computer.
old-location: termserv\itsgpolicyengine_isquarantineenabled.htm
old-project: termserv
ms.assetid: e63b99ba-068f-4842-b00a-9bfc5f8dac73
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITSGPolicyEngine interface [Remote Desktop Services],IsQuarantineEnabled method, ITSGPolicyEngine.IsQuarantineEnabled, ITSGPolicyEngine::IsQuarantineEnabled, IsQuarantineEnabled, IsQuarantineEnabled method [Remote Desktop Services], IsQuarantineEnabled method [Remote Desktop Services],ITSGPolicyEngine interface, termserv.itsgpolicyengine_isquarantineenabled, tsgpolicyengine/ITSGPolicyEngine::IsQuarantineEnabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tsgpolicyengine.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PolicyAttributeType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGPolicyEngine.IsQuarantineEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSGPolicyEngine::IsQuarantineEnabled


## -description


Indicates whether the authorization plug-in requires a statement of health (SoH) from the user's computer.


## -parameters




### -param quarantineEnabled [out]

Indicates whether the authorization plug-in requires a statement of health from the user's computer. <b>TRUE</b> to use RD Gateway to request an SoH from the user's computer; otherwise, <b>FALSE</b>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. If an error code is returned, RD Gateway assumes that an SoH is not required.




## -see-also




<a href="https://msdn.microsoft.com/1972032f-48ac-4a15-98ce-9349fa158a07">ITSGPolicyEngine</a>
 

 

