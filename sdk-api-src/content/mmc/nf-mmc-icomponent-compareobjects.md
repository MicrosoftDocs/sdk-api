---
UID: NF:mmc.IComponent.CompareObjects
title: IComponent::CompareObjects (mmc.h)
description: The IComponent::CompareObjects method enables a snap-in to compare two data objects acquired through IComponent::QueryDataObject. Be aware that data objects can be acquired from two different instances of IComponent.
helpviewer_keywords: ["CompareObjects","CompareObjects method [MMC]","CompareObjects method [MMC]","IComponent interface","IComponent interface [MMC]","CompareObjects method","IComponent.CompareObjects","IComponent::CompareObjects","_slate_icomponent_compareobjects","mmc.icomponent_compareobjects","mmc/IComponent::CompareObjects"]
old-location: mmc\icomponent_compareobjects.htm
tech.root: mmc
ms.assetid: 5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a
ms.date: 12/05/2018
ms.keywords: CompareObjects, CompareObjects method [MMC], CompareObjects method [MMC],IComponent interface, IComponent interface [MMC],CompareObjects method, IComponent.CompareObjects, IComponent::CompareObjects, _slate_icomponent_compareobjects, mmc.icomponent_compareobjects, mmc/IComponent::CompareObjects
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
 - IComponent::CompareObjects
 - mmc/IComponent::CompareObjects
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
 - IComponent.CompareObjects
---

# IComponent::CompareObjects


## -description

The <b>IComponent::CompareObjects</b> method enables a snap-in to compare two data objects acquired through 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>.

## -parameters

### -param lpDataObjectA [in]

A pointer to the first object exposing an IDataObject interface that is to be compared.

### -param lpDataObjectB [in]

A pointer to the second object exposing an IDataObject interface that is to be compared.

## -returns

This method can return one of these values.

## -remarks

The 
IDataObject interface is documented in the Platform Software Development Kit (SDK).

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>