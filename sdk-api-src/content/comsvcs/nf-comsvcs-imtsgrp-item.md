---
UID: NF:comsvcs.IMtsGrp.Item
title: IMtsGrp::Item
author: windows-sdk-content
description: Retrieves the IUnknown pointer for the specified package.
old-location: cos\imtsgrp_item.htm
old-project: cossdk
ms.assetid: 6360f38d-43e2-4b78-a9f5-9a525d4c596a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMtsGrp interface [COM+],Item method, IMtsGrp.Item, IMtsGrp::Item, Item, Item method [COM+], Item method [COM+],IMtsGrp interface, _dtc_IMtsGrp_Item, comsvcs/IMtsGrp::Item, cos.imtsgrp_item
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsGrp.Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMtsGrp::Item


## -description


Retrieves the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer for the specified package.


## -parameters




### -param lIndex [in]

The index containing running packages.


### -param ppUnkDispatcher [out]

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer, which can be used to access <a href="https://msdn.microsoft.com/7db3a373-00d3-480e-8f8e-7e65a468d5dc">IMtsEvents</a>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/976b4f0a-79cb-4b2d-8d69-225230147c53">IMtsGrp</a>
 

 

