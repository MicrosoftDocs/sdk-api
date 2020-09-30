---
UID: NF:indexsrv.IColumnMapper.GetPropInfoFromName
title: IColumnMapper::GetPropInfoFromName (indexsrv.h)
description: Gets property information from a name. This will return a DBID pointer in parameter ppPropId which now has to be freed by the caller and not by the callee (this class).
helpviewer_keywords: ["GetPropInfoFromName","GetPropInfoFromName method [search]","GetPropInfoFromName method [search]","IColumnMapper interface","IColumnMapper interface [search]","GetPropInfoFromName method","IColumnMapper.GetPropInfoFromName","IColumnMapper::GetPropInfoFromName","indexsrv/IColumnMapper::GetPropInfoFromName","search.icolumnmapper_getpropinfofromname"]
old-location: search\icolumnmapper_getpropinfofromname.htm
tech.root: search
ms.assetid: F9306234-7CCC-412E-AA8C-7E8A04A8132F
ms.date: 12/05/2018
ms.keywords: GetPropInfoFromName, GetPropInfoFromName method [search], GetPropInfoFromName method [search],IColumnMapper interface, IColumnMapper interface [search],GetPropInfoFromName method, IColumnMapper.GetPropInfoFromName, IColumnMapper::GetPropInfoFromName, indexsrv/IColumnMapper::GetPropInfoFromName, search.icolumnmapper_getpropinfofromname
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
 - IColumnMapper::GetPropInfoFromName
 - indexsrv/IColumnMapper::GetPropInfoFromName
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
 - IColumnMapper.GetPropInfoFromName
---

# IColumnMapper::GetPropInfoFromName


## -description

Gets property information from a name. This will return a DBID pointer in parameter <i>ppPropId</i> which now has to be freed by the caller and not by the callee (this class).

## -parameters

### -param wcsPropName [in]

The property name to look up.

### -param ppPropId [out]

The return Id of the property.

### -param pPropType [out]

The return type of the property.

### -param puiWidth [out]

The return property width.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/indexsrv/nn-indexsrv-icolumnmapper">IColumnMapper</a>