---
UID: NF:mmc.IComponentData2.QueryDispatch
title: IComponentData2::QueryDispatch (mmc.h)
description: The QueryDispatch method returns the snap-in's IDispatch interface for a specified item.
helpviewer_keywords: ["CCT_RESULT = 0x8001","CCT_SCOPE = 0x8000","IComponentData2 interface [MMC]","QueryDispatch method","IComponentData2.QueryDispatch","IComponentData2::QueryDispatch","QueryDispatch","QueryDispatch method [MMC]","QueryDispatch method [MMC]","IComponentData2 interface","_slate_icomponentdata2_querydispatch","mmc.icomponentdata2_querydispatch","mmc/IComponentData2::QueryDispatch"]
old-location: mmc\icomponentdata2_querydispatch.htm
tech.root: mmc
ms.assetid: efff70f9-0226-4cf1-a6b3-475d90b379f9
ms.date: 12/05/2018
ms.keywords: CCT_RESULT = 0x8001, CCT_SCOPE = 0x8000, IComponentData2 interface [MMC],QueryDispatch method, IComponentData2.QueryDispatch, IComponentData2::QueryDispatch, QueryDispatch, QueryDispatch method [MMC], QueryDispatch method [MMC],IComponentData2 interface, _slate_icomponentdata2_querydispatch, mmc.icomponentdata2_querydispatch, mmc/IComponentData2::QueryDispatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponentData2::QueryDispatch
 - mmc/IComponentData2::QueryDispatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponentData2.QueryDispatch
---

# IComponentData2::QueryDispatch


## -description

The 
<b>QueryDispatch</b> method returns the snap-in's <b>IDispatch</b> interface for a specified item. MMC exposes this interface through the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation object model</a>. Script, or other applications, can access the <b>IDispatch</b> interface for the item represented by the specified cookie through the 
<a href="/previous-versions/windows/desktop/mmc/view-snapinscopeobject">View.SnapinScopeObject</a> and 
<a href="/previous-versions/windows/desktop/mmc/view-snapinselectionobject">View.SnapinSelectionObject</a> methods.

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

<a href="/previous-versions/windows/desktop/mmc/view-snapinscopeobject">View.SnapinScopeObject</a>



<a href="/previous-versions/windows/desktop/mmc/view-snapinselectionobject">View.SnapinSelectionObject</a>