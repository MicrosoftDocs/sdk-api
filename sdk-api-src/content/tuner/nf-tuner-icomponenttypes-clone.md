---
UID: NF:tuner.IComponentTypes.Clone
title: IComponentTypes::Clone
author: windows-sdk-content
description: The Clone method creates a new copy of the collection.
old-location: mstv\icomponenttypes_clone.htm
tech.root: mstv
ms.assetid: 4cc842fa-90bd-4618-8e67-36b15db50cd1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],Clone method, IComponentTypes.Clone, IComponentTypes::Clone, IComponentTypesClone, mstv.icomponenttypes_clone, tuner/IComponentTypes::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IComponentTypes.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentTypes::Clone


## -description



The <b>Clone</b> method creates a new copy of the collection.




## -parameters




### -param NewList

TBD




#### - ppNewList [out]

Address of an <b>IComponentTypes</b> interface pointer that will be set to the new <a href="https://msdn.microsoft.com/b0a468fd-6294-4148-a727-3a4bd51df6dc">ComponentTypes</a> object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

