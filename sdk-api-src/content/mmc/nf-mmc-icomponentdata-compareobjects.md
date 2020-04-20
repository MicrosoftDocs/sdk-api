---
UID: NF:mmc.IComponentData.CompareObjects
title: IComponentData::CompareObjects (mmc.h)
description: The IComponentData::CompareObjects method enables a snap-in to compare two data objects acquired through QueryDataObject. Be aware that the data objects can be acquired from two different instances of IComponentData.helpviewer_keywords: ["CompareObjects","CompareObjects method [MMC]","CompareObjects method [MMC]","IComponentData interface","IComponentData interface [MMC]","CompareObjects method","IComponentData.CompareObjects","IComponentData::CompareObjects","_slate_icomponentdata_compareobjects","mmc.icomponentdata_compareobjects","mmc/IComponentData::CompareObjects"]
old-location: mmc\icomponentdata_compareobjects.htm
tech.root: mmc
ms.assetid: d6ca3957-3d0c-492d-9e47-fc898981720b
ms.date: 12/05/2018
ms.keywords: CompareObjects, CompareObjects method [MMC], CompareObjects method [MMC],IComponentData interface, IComponentData interface [MMC],CompareObjects method, IComponentData.CompareObjects, IComponentData::CompareObjects, _slate_icomponentdata_compareobjects, mmc.icomponentdata_compareobjects, mmc/IComponentData::CompareObjects
f1_keywords:
- mmc/IComponentData.CompareObjects
dev_langs:
- c++
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
- IComponentData.CompareObjects
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentData::CompareObjects


## -description


The <b>IComponentData::CompareObjects</b> method enables a snap-in to compare two data objects acquired through 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponentdata-querydataobject">QueryDataObject</a>. Be aware that the data objects can be acquired from two different instances of 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>.


## -parameters




### -param lpDataObjectA [in]

A pointer to the first data object exposing an 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface that is to be compared.


### -param lpDataObjectB [in]

A pointer to the second data object exposing an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface that is to be compared.


## -returns



This method can return one of these values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>
 

 

