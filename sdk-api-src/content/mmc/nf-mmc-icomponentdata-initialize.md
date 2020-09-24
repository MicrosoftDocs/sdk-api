---
UID: NF:mmc.IComponentData.Initialize
title: IComponentData::Initialize (mmc.h)
description: The IComponentData::Initialize method provides an entry point to the console.
helpviewer_keywords: ["IComponentData interface [MMC]","Initialize method","IComponentData.Initialize","IComponentData::Initialize","Initialize","Initialize method [MMC]","Initialize method [MMC]","IComponentData interface","_slate_icomponentdata_initialize","mmc.icomponentdata_initialize","mmc/IComponentData::Initialize"]
old-location: mmc\icomponentdata_initialize.htm
tech.root: mmc
ms.assetid: 7893b3d6-f576-41cc-bbe5-2fcef7c327d7
ms.date: 12/05/2018
ms.keywords: IComponentData interface [MMC],Initialize method, IComponentData.Initialize, IComponentData::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],IComponentData interface, _slate_icomponentdata_initialize, mmc.icomponentdata_initialize, mmc/IComponentData::Initialize
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
 - IComponentData::Initialize
 - mmc/IComponentData::Initialize
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
 - IComponentData.Initialize
---

# IComponentData::Initialize


## -description

The <b>IComponentData::Initialize</b> method provides an entry point to the console.

## -parameters

### -param pUnknown [in]

A pointer to the console IUnknown interface. This interface pointer can be used to call QueryInterface for 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> and 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>.

## -returns

This method can return one of these values.

## -remarks

<b>IComponentData::Initialize</b> is called when a snap-in is created and has items to enumerate in the scope pane. The pointer to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> that is passed in is used to make <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> calls to the console for interfaces such as 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> and 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNamespace2</a>. The snap-in should also call 
<a href="/previous-versions/windows/desktop/legacy/aa814791(v=vs.85)">IConsole2::QueryScopeImageList</a> to get the image list for the scope pane and add images to be displayed on the scope pane side.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>