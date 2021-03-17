---
UID: NF:ole2.OleConvertIStorageToOLESTREAMEx
title: OleConvertIStorageToOLESTREAMEx function (ole2.h)
description: The OleConvertIStorageToOLESTREAMEx function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model, including the presentation data.
helpviewer_keywords: ["OleConvertIStorageToOLESTREAMEx","OleConvertIStorageToOLESTREAMEx function [Structured Storage]","_stg_oleconvertistoragetoolestreamex","ole2/OleConvertIStorageToOLESTREAMEx","stg.oleconvertistoragetoolestreamex"]
old-location: stg\oleconvertistoragetoolestreamex.htm
tech.root: Stg
ms.assetid: a6026b71-4223-40ab-b209-44531480db57
ms.date: 12/05/2018
ms.keywords: OleConvertIStorageToOLESTREAMEx, OleConvertIStorageToOLESTREAMEx function [Structured Storage], _stg_oleconvertistoragetoolestreamex, ole2/OleConvertIStorageToOLESTREAMEx, stg.oleconvertistoragetoolestreamex
req.header: ole2.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleConvertIStorageToOLESTREAMEx
 - ole2/OleConvertIStorageToOLESTREAMEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleConvertIStorageToOLESTREAMEx
---

# OleConvertIStorageToOLESTREAMEx function


## -description

The 
<b>OleConvertIStorageToOLESTREAMEx</b> function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model, including the presentation data. This is one of several functions included in Structured Storage to ensure compatibility between OLE1 and OLE2.

## -parameters

### -param pstg [in]

Pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object to be converted to an OLE 1 storage.

### -param cfFormat [in]

Format of the presentation data. May be <b>NULL</b>, in which case the <i>lWidth</i>, <i>lHeight</i>, <i>dwSize</i>, and <i>pmedium</i> parameters are ignored.

### -param lWidth [in]

Width of the object presentation data in HIMETRIC units.

### -param lHeight [in]

Height of the object presentation data in HIMETRIC units.

### -param dwSize [in]

Size of the data, in bytes, to be converted.

### -param pmedium [in]

Pointer to the 
<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure for the serialized data to be converted.

### -param polestm [out]

Pointer to a stream where the persistent representation of the object is saved using the OLE 1 storage model.

## -returns

This function supports the standard return value E_INVALIDARG, in addition to the following:

## -remarks

The 
<b>OleConvertIStorageToOLESTREAMEx</b> function converts an OLE 2 storage object to OLE 1 format. It differs from the 
<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestream">OleConvertIStorageToOLESTREAM</a> function in that the 
<b>OleConvertIStorageToOLESTREAMEx</b> function also passes the presentation data to the OLE 1 storage object, whereas the 
<b>OleConvertIStorageToOLESTREAM</b> function does not.

Because 
<b>OleConvertIStorageToOLESTREAMEx</b> can specify which presentation data to convert, it can be used by applications that do not use OLE default caching resources but do use OLE's conversion resources.

The value of the <b>tymed</b> member of 
<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> must be either TYMED_HGLOBAL or TYMED_ISTREAM; refer to the 
<a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a> enumeration for more information. The medium is not released by the 
<b>OleConvertIStorageToOLESTREAMEx</b> function.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coisole1class">CoIsOle1Class</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestream">OleConvertIStorageToOLESTREAM</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorage">OleConvertOLESTREAMToIStorage</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorageex">OleConvertOLESTREAMToIStorageEx</a>



<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a>



<a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a>