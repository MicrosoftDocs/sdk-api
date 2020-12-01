---
UID: NF:ole2.OleConvertOLESTREAMToIStorageEx
title: OleConvertOLESTREAMToIStorageEx function (ole2.h)
description: The OleConvertOLESTREAMToIStorageEx function converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object including presentation data. This is one of several compatibility functions.
helpviewer_keywords: ["OleConvertOLESTREAMToIStorageEx","OleConvertOLESTREAMToIStorageEx function [Structured Storage]","_stg_oleconvertolestreamtoistorageex","ole2/OleConvertOLESTREAMToIStorageEx","stg.oleconvertolestreamtoistorageex"]
old-location: stg\oleconvertolestreamtoistorageex.htm
tech.root: Stg
ms.assetid: 2e77fa0e-1d98-4c59-8d3c-65bd7235ec8f
ms.date: 12/05/2018
ms.keywords: OleConvertOLESTREAMToIStorageEx, OleConvertOLESTREAMToIStorageEx function [Structured Storage], _stg_oleconvertolestreamtoistorageex, ole2/OleConvertOLESTREAMToIStorageEx, stg.oleconvertolestreamtoistorageex
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
 - OleConvertOLESTREAMToIStorageEx
 - ole2/OleConvertOLESTREAMToIStorageEx
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
 - OleConvertOLESTREAMToIStorageEx
---

# OleConvertOLESTREAMToIStorageEx function


## -description

The 
<b>OleConvertOLESTREAMToIStorageEx</b> function converts the specified object from the OLE 1 storage model to an OLE 2 structured storage object including presentation data. This is one of several compatibility functions.

## -parameters

### -param polestm [in]

Pointer to the stream that contains the persistent representation of the object in the OLE 1 storage format.

### -param pstg [out]

Pointer to the OLE 2 structured storage object.

### -param pcfFormat [out]

Pointer to where the format of the presentation data is returned. May be <b>NULL</b>, indicating the absence of presentation data.

### -param plwWidth [out]

Pointer to where the width value (in HIMETRIC) of the presentation data is returned.

### -param plHeight [out]

Pointer to where the height value (in HIMETRIC) of the presentation data is returned.

### -param pdwSize [out]

Pointer to where the size in bytes of the converted data is returned.

### -param pmedium [out]

Pointer to where the 
<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure for the converted serialized data is returned.

## -returns

This function returns HRESULT.

## -remarks

This function converts an OLE 1 object to an OLE 2 structured storage object. You can use this function to update OLE 1 objects to OLE 2 objects when a new version of the object application supports OLE 2.

This function differs from the 
<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorage">OleConvertOLESTREAMToIStorage</a> function in that the presentation data read from the <b>OLESTREAM</b> structure is passed out and the newly created OLE 2 storage object does not contain a presentation stream.

Since this function can specify which presentation data to convert, it can be used by applications that do not use OLE's default caching resources but do use the conversion resources.

The <b>tymed</b> member of 
<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> can only be TYMED_NULL or TYMED_ISTREAM. If it is TYMED_NULL, the data will be returned in a global handle through the <b>hGlobal</b> member of <b>STGMEDIUM</b>, otherwise data will be written into the <b>pstm</b> member of this structure.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coisole1class">CoIsOle1Class</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestream">OleConvertIStorageToOLESTREAM</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestreamex">OleConvertIStorageToOLESTREAMEx</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorage">OleConvertOLESTREAMToIStorage</a>



<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a>



<a href="/windows/desktop/api/objidl/ne-objidl-tymed">TYMED</a>