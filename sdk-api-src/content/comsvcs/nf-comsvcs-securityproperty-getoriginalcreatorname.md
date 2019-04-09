---
UID: NF:comsvcs.SecurityProperty.GetOriginalCreatorName
title: SecurityProperty::GetOriginalCreatorName (comsvcs.h)
author: windows-sdk-content
description: Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.
old-location: cos\securityproperty_getoriginalcreatorname.htm
tech.root: cossdk
ms.assetid: 403f0f36-f386-4eeb-905a-e04c5699db9b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOriginalCreatorName, GetOriginalCreatorName method [COM+], GetOriginalCreatorName method [COM+],SecurityProperty interface, SecurityProperty interface [COM+],GetOriginalCreatorName method, SecurityProperty.GetOriginalCreatorName, SecurityProperty::GetOriginalCreatorName, _cos_SecurityProperty_GetOriginalCreatorName, comsvcs/SecurityProperty::GetOriginalCreatorName, cos.securityproperty_getoriginalcreatorname
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - SecurityProperty.GetOriginalCreatorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SecurityProperty::GetOriginalCreatorName


## -description


<p class="CCE_Message">[Do not use this method in COM+ applications because it was designed to be used only in MTS 2.0 applications.]

Retrieves the user name associated with the original base process that initiated the activity in which the current object is executing.


## -parameters




### -param bstrUserName [out]

A reference to the user name associated with the original base process that initiated the activity in which the current object is executing.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3">SecurityProperty</a>
 

 

