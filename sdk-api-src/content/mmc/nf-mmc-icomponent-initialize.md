---
UID: NF:mmc.IComponent.Initialize
title: IComponent::Initialize (mmc.h)
description: The IComponent::Initialize method provides an entry point to the console.
helpviewer_keywords: ["IComponent interface [MMC]","Initialize method","IComponent.Initialize","IComponent::Initialize","Initialize","Initialize method [MMC]","Initialize method [MMC]","IComponent interface","_slate_icomponent_initialize","mmc.icomponent_initialize","mmc/IComponent::Initialize"]
old-location: mmc\icomponent_initialize.htm
tech.root: mmc
ms.assetid: 2a8b8f79-05c0-49e8-8210-7c1002ee5978
ms.date: 12/05/2018
ms.keywords: IComponent interface [MMC],Initialize method, IComponent.Initialize, IComponent::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],IComponent interface, _slate_icomponent_initialize, mmc.icomponent_initialize, mmc/IComponent::Initialize
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
 - IComponent::Initialize
 - mmc/IComponent::Initialize
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
 - IComponent.Initialize
---

# IComponent::Initialize


## -description

The <b>IComponent::Initialize</b> method provides an entry point to the console. At this point, the snap-in should set up the toolbar. If the snap-in uses the default list view it should also set up the list view's headers and add images to be used in the result pane.

## -parameters

### -param lpConsole [in]

A pointer to the console 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole</a> interface.

## -returns

This method can return one of these values.

## -remarks

<b>IComponent::Initialize</b> is called when a snap-in is being created. The pointer to IConsole that is passed in is used to make QueryInterface calls to the console for interfaces such as 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>. You can also call QueryInterface on the IConsole pointer to get an 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> interface pointer.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">IComponent::Destroy</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>