---
UID: NF:mmc.IComponentData2.QueryDispatch
title: IComponentData2::QueryDispatch
author: windows-sdk-content
description: The QueryDispatch method returns the snap-in's IDispatch interface for a specified item.
old-location: mmc\icomponentdata2_querydispatch.htm
old-project: MMC
ms.assetid: efff70f9-0226-4cf1-a6b3-475d90b379f9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CCT_RESULT = 0x8001, CCT_SCOPE = 0x8000, IComponentData2 interface [MMC],QueryDispatch method, IComponentData2.QueryDispatch, IComponentData2::QueryDispatch, QueryDispatch, QueryDispatch method [MMC], QueryDispatch method [MMC],IComponentData2 interface, _slate_icomponentdata2_querydispatch, mmc.icomponentdata2_querydispatch, mmc/IComponentData2::QueryDispatch
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponentData2.QueryDispatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponentData2::QueryDispatch


## -description


The 
<b>QueryDispatch</b> method returns the snap-in's <b>IDispatch</b> interface for a specified item. MMC exposes this interface through the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation object model</a>. Script, or other applications, can access the <b>IDispatch</b> interface for the item represented by the specified cookie through the 
<a href="https://msdn.microsoft.com/340ab6d0-e674-438a-9c84-87dcb274ae6a">View.SnapinScopeObject</a> and 
<a href="https://msdn.microsoft.com/f29347ab-9339-4e77-95a7-c9fb7992e676">View.SnapinSelectionObject</a> methods.


## -parameters




### -param cookie [in]

A value that specifies the context item (or items) for which the <b>IDispatch</b> interface is requested. The <i>cookie</i> value is previously provided by the snap-in, and MMC uses it in this method call.


### -param type [in]

A value that specifies the data object as one of the following constant values, which are members of the 
<b>DATA_OBJECT_TYPES</b> enumeration.



#### CCT_SCOPE = 0x8000

Data object for the scope pane.



#### CCT_RESULT = 0x8001

Data object for the result pane.


### -param ppDispatch [out]

Dispatch interface pointer. The snap-in sets *<i>ppDispatch</i> to the <b>IDispatch</b> interface corresponding to the <i>cookie</i> value.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.




## -see-also




<a href="https://msdn.microsoft.com/340ab6d0-e674-438a-9c84-87dcb274ae6a">View.SnapinScopeObject</a>



<a href="https://msdn.microsoft.com/f29347ab-9339-4e77-95a7-c9fb7992e676">View.SnapinSelectionObject</a>
 

 

