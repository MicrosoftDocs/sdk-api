---
UID: NF:mmc.IComponent2.QueryDispatch
title: IComponent2::QueryDispatch
author: windows-sdk-content
description: The QueryDispatch method returns the snap-in IDispatch interface for a specified item.
old-location: mmc\icomponent2_querydispatch.htm
tech.root: mmc
ms.assetid: 42c43111-7d65-4cfc-bb14-6a5d06f694e7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CCT_RESULT = 0x8001, CCT_SCOPE = 0x8000, IComponent2 interface [MMC],QueryDispatch method, IComponent2.QueryDispatch, IComponent2::QueryDispatch, QueryDispatch, QueryDispatch method [MMC], QueryDispatch method [MMC],IComponent2 interface, _slate_icomponent2_querydispatch, mmc.icomponent2_querydispatch, mmc/IComponent2::QueryDispatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Mmc.h
api_name:
 - IComponent2.QueryDispatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IComponent2.QueryDispatch
: 
---

# IComponent2::QueryDispatch


## -description


The 
QueryDispatch method returns the snap-in IDispatch interface for a specified item. MMC will expose this interface through the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation object model</a>. Script, or other applications, can access the IDispatch interface for the item represented by the specified cookie through the 
<a href="https://msdn.microsoft.com/340ab6d0-e674-438a-9c84-87dcb274ae6a">View.SnapinScopeObject</a> and 
<a href="https://msdn.microsoft.com/f29347ab-9339-4e77-95a7-c9fb7992e676">View.SnapinSelectionObject</a> methods.


## -parameters




### -param cookie [in]

A value that specifies the context item (or items) for which the IDispatch interface is requested. The cookie value is previously provided by the snap-in, and MMC uses it in this method call.


### -param type [in]

A value that specifies the data object as one of the following constant values, which, are members of the 
<a href="https://msdn.microsoft.com/6f1cb622-b066-4208-9e25-cdd7e9c4dcd2">DATA_OBJECT_TYPES</a> enumeration.



#### CCT_SCOPE = 0x8000

Data object for the scope pane.



#### CCT_RESULT = 0x8001

Data object for the result pane.


### -param ppDispatch [out]

A dispatch interface pointer. The snap-in sets *ppDispatch to the IDispatch interface that corresponds  to the cookie value.


## -returns



If successful, the return value is <b>S_OK</b>. Other return values indicate an error code.




## -see-also




<a href="https://msdn.microsoft.com/340ab6d0-e674-438a-9c84-87dcb274ae6a">View.SnapinScopeObject</a>



<a href="https://msdn.microsoft.com/f29347ab-9339-4e77-95a7-c9fb7992e676">View.SnapinSelectionObject</a>
 

 

