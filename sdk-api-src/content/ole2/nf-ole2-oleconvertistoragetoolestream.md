---
UID: NF:ole2.OleConvertIStorageToOLESTREAM
title: OleConvertIStorageToOLESTREAM function (ole2.h)
description: The OleConvertIStorageToOLESTREAM function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model but does not include the presentation data. This is one of several compatibility functions.
helpviewer_keywords: ["OleConvertIStorageToOLESTREAM","OleConvertIStorageToOLESTREAM function [Structured Storage]","_stg_oleconvertistoragetoolestream","ole2/OleConvertIStorageToOLESTREAM","stg.oleconvertistoragetoolestream"]
old-location: stg\oleconvertistoragetoolestream.htm
tech.root: Stg
ms.assetid: d100d32a-6559-4a7c-a0ae-780bc9d82611
ms.date: 12/05/2018
ms.keywords: OleConvertIStorageToOLESTREAM, OleConvertIStorageToOLESTREAM function [Structured Storage], _stg_oleconvertistoragetoolestream, ole2/OleConvertIStorageToOLESTREAM, stg.oleconvertistoragetoolestream
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
 - OleConvertIStorageToOLESTREAM
 - ole2/OleConvertIStorageToOLESTREAM
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
 - OleConvertIStorageToOLESTREAM
---

# OleConvertIStorageToOLESTREAM function


## -description

The 
<b>OleConvertIStorageToOLESTREAM</b> function converts the specified storage object from OLE 2 structured storage to the OLE 1 storage object model but does not include the presentation data. This is one of several compatibility functions.

## -parameters

### -param pstg [in]

Pointer to the 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object to be converted to an OLE 1 storage.

### -param lpolestream [out]

Pointer to an OLE 1 stream structure where the persistent representation of the object is saved using the OLE 1 storage model.

## -returns

This function supports the standard return value E_INVALIDARG, in addition to the following:

## -remarks

This function converts an OLE 2 storage object to OLE 1 format. The <b>OLESTREAM</b> structure code implemented for OLE 1 must be available.

On entry, the stream to which <i>lpolestm</i> points should be created and positioned just as it would be for an 
<a href="/windows/desktop/api/ole/nf-ole-olesavetostream">OleSaveToStream</a> call. On exit, the stream contains the persistent representation of the object using OLE 1 storage.

<div class="alert"><b>Note</b>  Paintbrush objects are dealt with differently from other objects because their native data is in device-independent bitmap (DIB) format. When Paintbrush objects are converted using 
<b>OleConvertIStorageToOLESTREAM</b>, no presentation data is added to the <b>OLESTREAM</b> structure. To include presentation data, use the 
<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestreamex">OleConvertIStorageToOLESTREAMEx</a> function instead.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coisole1class">CoIsOle1Class</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertistoragetoolestreamex">OleConvertIStorageToOLESTREAMEx</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorage">OleConvertOLESTREAMToIStorage</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleconvertolestreamtoistorageex">OleConvertOLESTREAMToIStorageEx</a>