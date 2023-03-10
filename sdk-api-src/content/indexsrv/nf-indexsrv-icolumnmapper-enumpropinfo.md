---
UID: NF:indexsrv.IColumnMapper.EnumPropInfo
title: IColumnMapper::EnumPropInfo (indexsrv.h)
description: Gets the i-th entry from the list of properties.
helpviewer_keywords: ["EnumPropInfo","EnumPropInfo method [search]","EnumPropInfo method [search]","IColumnMapper interface","IColumnMapper interface [search]","EnumPropInfo method","IColumnMapper.EnumPropInfo","IColumnMapper::EnumPropInfo","indexsrv/IColumnMapper::EnumPropInfo","search.icolumnmapper_enumpropinfo"]
old-location: search\icolumnmapper_enumpropinfo.htm
tech.root: search
ms.assetid: E24E7258-1A5D-4FA0-8F17-6E2B00582AF3
ms.date: 12/05/2018
ms.keywords: EnumPropInfo, EnumPropInfo method [search], EnumPropInfo method [search],IColumnMapper interface, IColumnMapper interface [search],EnumPropInfo method, IColumnMapper.EnumPropInfo, IColumnMapper::EnumPropInfo, indexsrv/IColumnMapper::EnumPropInfo, search.icolumnmapper_enumpropinfo
req.header: indexsrv.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
f1_keywords:
 - IColumnMapper::EnumPropInfo
 - indexsrv/IColumnMapper::EnumPropInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - indexsrv.h
api_name:
 - IColumnMapper.EnumPropInfo
---

# IColumnMapper::EnumPropInfo


## -description

Gets the i-th entry from the list of properties.

## -parameters

### -param iEntry [in]

i-th entry to retrieve. Note that the entries are 0-based.

### -param pwcsName [out]

The return property name.

### -param ppPropId [out]

The Id of the property.

### -param pPropType [out]

The return type of the property.

### -param puiWidth [out]

The return property width.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-icolumnmapper">IColumnMapper</a>