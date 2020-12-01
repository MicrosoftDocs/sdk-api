---
UID: NF:mmc.IComponentData.CreateComponent
title: IComponentData::CreateComponent (mmc.h)
description: The IComponentData::CreateComponent method creates an instance of the IComponent that will be associated with this IComponentData interface.
helpviewer_keywords: ["CreateComponent","CreateComponent method [MMC]","CreateComponent method [MMC]","IComponentData interface","IComponentData interface [MMC]","CreateComponent method","IComponentData.CreateComponent","IComponentData::CreateComponent","_slate_icomponentdata_createcomponent","mmc.icomponentdata_createcomponent","mmc/IComponentData::CreateComponent"]
old-location: mmc\icomponentdata_createcomponent.htm
tech.root: mmc
ms.assetid: cb9e7ccb-8431-4f12-a8da-648410ff3da6
ms.date: 12/05/2018
ms.keywords: CreateComponent, CreateComponent method [MMC], CreateComponent method [MMC],IComponentData interface, IComponentData interface [MMC],CreateComponent method, IComponentData.CreateComponent, IComponentData::CreateComponent, _slate_icomponentdata_createcomponent, mmc.icomponentdata_createcomponent, mmc/IComponentData::CreateComponent
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
 - IComponentData::CreateComponent
 - mmc/IComponentData::CreateComponent
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
 - IComponentData.CreateComponent
---

# IComponentData::CreateComponent


## -description

The <b>IComponentData::CreateComponent</b> method creates an instance of the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> that will be associated with this 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a> interface.

## -parameters

### -param ppComponent [out]

A pointer to the location that stores the newly created pointer to 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>