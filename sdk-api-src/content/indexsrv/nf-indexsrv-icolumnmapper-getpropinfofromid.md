---
UID: NF:indexsrv.IColumnMapper.GetPropInfoFromId
title: IColumnMapper::GetPropInfoFromId (indexsrv.h)
description: Gets the property information from the DBID.
helpviewer_keywords: ["GetPropInfoFromId","GetPropInfoFromId method [search]","GetPropInfoFromId method [search]","IColumnMapper interface","IColumnMapper interface [search]","GetPropInfoFromId method","IColumnMapper.GetPropInfoFromId","IColumnMapper::GetPropInfoFromId","indexsrv/IColumnMapper::GetPropInfoFromId","search.icolumnmapper_getpropinfofromid"]
old-location: search\icolumnmapper_getpropinfofromid.htm
tech.root: search
ms.assetid: 94E7A6B4-0EA9-40F4-B69B-B1A30B0B5229
ms.date: 12/05/2018
ms.keywords: GetPropInfoFromId, GetPropInfoFromId method [search], GetPropInfoFromId method [search],IColumnMapper interface, IColumnMapper interface [search],GetPropInfoFromId method, IColumnMapper.GetPropInfoFromId, IColumnMapper::GetPropInfoFromId, indexsrv/IColumnMapper::GetPropInfoFromId, search.icolumnmapper_getpropinfofromid
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
 - IColumnMapper::GetPropInfoFromId
 - indexsrv/IColumnMapper::GetPropInfoFromId
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
 - IColumnMapper.GetPropInfoFromId
---

# IColumnMapper::GetPropInfoFromId


## -description

Gets the property information from the DBID.

## -parameters

### -param pPropId [in]

Pointer to the property to look up.

### -param pwcsName [out]

The return property name.

### -param pPropType [out]

The return type of the property.

### -param puiWidth [out]

The return property width.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-icolumnmapper">IColumnMapper</a>