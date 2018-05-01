---
UID: NF:comsvcs.SecurityProperty.GetDirectCreatorName
title: SecurityProperty::GetDirectCreatorName method
author: windows-driver-content
description: Retrieves the user name associated with the current object's immediate (out-of-process) creator.
old-location: cos\securityproperty_getdirectcreatorname.htm
old-project: cossdk
ms.assetid: 26619719-bcca-4776-9580-edc541e6b821
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetDirectCreatorName method [COM+], GetDirectCreatorName method [COM+], SecurityProperty interface, GetDirectCreatorName,SecurityProperty.GetDirectCreatorName, SecurityProperty, SecurityProperty interface [COM+], GetDirectCreatorName method, SecurityProperty::GetDirectCreatorName, _cos_SecurityProperty_GetDirectCreatorName, comsvcs/SecurityProperty::GetDirectCreatorName, cos.securityproperty_getdirectcreatorname
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	SecurityProperty.GetDirectCreatorName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SecurityProperty::GetDirectCreatorName method


## -description


<p class="CCE_Message">[Do not use this method in COM+ applications because it was designed to be used only in MTS 2.0 applications.]

Retrieves the user name associated with the current object's immediate (out-of-process) creator.


## -parameters




### -param bstrUserName [out]

A reference to the user name associated with the current object's immediate (out-of-process) creator.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3">SecurityProperty</a>
 

 

