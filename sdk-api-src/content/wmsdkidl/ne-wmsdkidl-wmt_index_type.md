---
UID: NE:wmsdkidl.tagWMT_INDEX_TYPE
title: WMT_INDEX_TYPE (wmsdkidl.h)
description: The WMT_INDEX_TYPE enumeration type defines the type of object that will be associated with an index.
helpviewer_keywords: ["WMT_INDEX_TYPE","WMT_INDEX_TYPE enumeration [windows Media Format]","WMT_IT_NEAREST_CLEAN_POINT","WMT_IT_NEAREST_DATA_UNIT","WMT_IT_NEAREST_OBJECT","wmformat.wmt_index_type","wmsdkidl/WMT_INDEX_TYPE","wmsdkidl/WMT_IT_NEAREST_CLEAN_POINT","wmsdkidl/WMT_IT_NEAREST_DATA_UNIT","wmsdkidl/WMT_IT_NEAREST_OBJECT"]
old-location: wmformat\wmt_index_type.htm
tech.root: wmformat
ms.assetid: 250f12ba-2334-41e4-9258-0da79dd4cb3d
ms.date: 12/05/2018
ms.keywords: WMT_INDEX_TYPE, WMT_INDEX_TYPE enumeration [windows Media Format], WMT_IT_NEAREST_CLEAN_POINT, WMT_IT_NEAREST_DATA_UNIT, WMT_IT_NEAREST_OBJECT, wmformat.wmt_index_type, wmsdkidl/WMT_INDEX_TYPE, wmsdkidl/WMT_IT_NEAREST_CLEAN_POINT, wmsdkidl/WMT_IT_NEAREST_DATA_UNIT, wmsdkidl/WMT_IT_NEAREST_OBJECT
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WMT_INDEX_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMT_INDEX_TYPE
 - wmsdkidl/tagWMT_INDEX_TYPE
 - WMT_INDEX_TYPE
 - wmsdkidl/WMT_INDEX_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_INDEX_TYPE
---

# WMT_INDEX_TYPE enumeration


## -description

The <b>WMT_INDEX_TYPE</b> enumeration type defines the type of object that will be associated with an index. Because the time specified by an index will not usually correspond exactly with an object in the file, the indexer must associate the index with an object in the bit stream close to the specified time.

## -enum-fields

### -field WMT_IT_NEAREST_DATA_UNIT:1

The index will associate indexes with the nearest data unit, or packet, in the Windows Media file.

### -field WMT_IT_NEAREST_OBJECT

The index will associate indexes with the nearest data object, or compressed sample, in the Windows Media file.

### -field WMT_IT_NEAREST_CLEAN_POINT

The index will associate indexes with the nearest <a href="/windows/desktop/wmformat/wmformat-glossary">cleanpoint</a>, or video key frame, in the Windows Media file. This is the default index type.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
