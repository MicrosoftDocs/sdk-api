---
UID: NF:mmc.IComponentData.QueryDataObject
title: IComponentData::QueryDataObject (mmc.h)
description: The IComponentData::QueryDataObject method returns a data object that can be used to retrieve the context information for the specified cookie.
helpviewer_keywords: ["CCT_RESULT = 0x8001","CCT_SCOPE = 0x8000","CCT_SNAPIN_MANAGER = 0x8002","CCT_UNINITIALIZED = 0xFFFF","IComponentData interface [MMC]","QueryDataObject method","IComponentData.QueryDataObject","IComponentData::QueryDataObject","QueryDataObject","QueryDataObject method [MMC]","QueryDataObject method [MMC]","IComponentData interface","_slate_icomponentdata_querydataobject","mmc.icomponentdata_querydataobject","mmc/IComponentData::QueryDataObject"]
old-location: mmc\icomponentdata_querydataobject.htm
tech.root: mmc
ms.assetid: 567d068e-5447-438c-9719-93227807263a
ms.date: 12/05/2018
ms.keywords: CCT_RESULT = 0x8001, CCT_SCOPE = 0x8000, CCT_SNAPIN_MANAGER = 0x8002, CCT_UNINITIALIZED = 0xFFFF, IComponentData interface [MMC],QueryDataObject method, IComponentData.QueryDataObject, IComponentData::QueryDataObject, QueryDataObject, QueryDataObject method [MMC], QueryDataObject method [MMC],IComponentData interface, _slate_icomponentdata_querydataobject, mmc.icomponentdata_querydataobject, mmc/IComponentData::QueryDataObject
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
 - IComponentData::QueryDataObject
 - mmc/IComponentData::QueryDataObject
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
 - IComponentData.QueryDataObject
---

# IComponentData::QueryDataObject


## -description

The <b>IComponentData::QueryDataObject</b> method returns a data object that can be used to retrieve the context information for the specified cookie.

## -parameters

### -param cookie [in]

A value that specifies the unique identifier for which the data object is required.

### -param type [in]

A value that specifies the data object as one of the following:



#### CCT_SCOPE = 0x8000

Data object for the scope pane.



#### CCT_RESULT = 0x8001

Data object for the result pane.



#### CCT_SNAPIN_MANAGER = 0x8002

Data object for the Snap-In Manager context.



#### CCT_UNINITIALIZED = 0xFFFF

Data object has an invalid type.

These constants are members of the 
<a href="/windows/desktop/api/mmc/ne-mmc-data_object_types">DATA_OBJECT_TYPES</a> enumeration.

### -param ppDataObject [out]

A pointer to the address of the returned data object.

## -returns

This method can return one of these values.

## -remarks

You can pass these data objects to the same snap-in or to extension snap-ins that require them. Some of the MMC interfaces that can use this data object are 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>, 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>, 
<a href="/windows/desktop/api/mmc/nn-mmc-icontextmenuprovider">IContextMenuProvider</a>, 
<a href="/windows/desktop/api/mmc/nn-mmc-iextendcontextmenu">IExtendContextMenu</a>, 
<a href="/windows/desktop/api/mmc/nn-mmc-iextendpropertysheet2">IExtendPropertySheet2</a>, and 
<a href="/windows/desktop/api/mmc/nn-mmc-ipropertysheetprovider">IPropertySheetProvider</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>