---
UID: NF:tuner.IComponentTypes.Add
title: IComponentTypes::Add
author: windows-sdk-content
description: The Add method adds a new ComponentType object to the collection.
old-location: mstv\icomponenttypes_add.htm
old-project: mstv
ms.assetid: 157f8d81-dbbf-44a7-9786-0758d3c89634
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IComponentTypes interface, IComponentTypes interface [Microsoft TV Technologies],Add method, IComponentTypes.Add, IComponentTypes::Add, IComponentTypesAdd, mstv.icomponenttypes_add, tuner/IComponentTypes::Add
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponentTypes.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentTypes::Add


## -description



The <b>Add</b> method adds a new <a href="https://msdn.microsoft.com/d5d8af25-4d39-4327-bd6d-8984ae9e6a78">ComponentType</a> object to the collection.




## -parameters




### -param ComponentType




### -param NewIndex






#### - pComponentType [in]

Pointer to the <a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType</a> object that will be added to the collection.


#### - pNewIndex [out]

The index number of the component type after it has been added to the collection.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/47c3837b-1348-4359-ad3d-3d82c5fe3781">IComponentTypes Interface</a>
 

 

