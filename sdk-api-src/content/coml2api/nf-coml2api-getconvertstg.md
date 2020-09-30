---
UID: NF:coml2api.GetConvertStg
title: GetConvertStg function (coml2api.h)
description: The GetConvertStg function returns the current value of the convert bit for the specified storage object.
helpviewer_keywords: ["GetConvertStg","GetConvertStg function [Structured Storage]","_stg_getconvertstg","coml2api/GetConvertStg","stg.getconvertstg"]
old-location: stg\getconvertstg.htm
tech.root: Stg
ms.assetid: 748649a2-cf75-4ffa-ac1f-4a148b845d21
ms.date: 12/05/2018
ms.keywords: GetConvertStg, GetConvertStg function [Structured Storage], _stg_getconvertstg, coml2api/GetConvertStg, stg.getconvertstg
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetConvertStg
 - coml2api/GetConvertStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - GetConvertStg
---

# GetConvertStg function


## -description

The 
<b>GetConvertStg</b> function returns the current value of the convert bit for the specified storage object.

## -parameters

### -param pStg [in]

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the storage object from which the convert bit is to be retrieved.

## -returns

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstream">IStorage::OpenStream</a>, 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstorage">IStorage::OpenStorage</a>, and 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> storage and stream access errors.

## -remarks

The 
<b>GetConvertStg</b> function is called by object servers that support the conversion of an object from one format to another. The server must be able to read the storage object using the format of its previous class identifier (CLSID) and write the object using the format of its new CLSID to support the object's conversion. For example, a spreadsheet created by one application can be converted to the format used by a different application.

The convert bit is set by a call to the 
<a href="/windows/desktop/api/ole2/nf-ole2-setconvertstg">SetConvertStg</a> function. A container application can call this function on the request of an end user, or a setup program can call it when installing a new version of an application. An end user requests converting an object through the <b>Convert To</b> dialog box. When an object is converted, the new CLSID is permanently assigned to the object, so the object is subsequently associated with the new CLSID.

Then, when the object is activated, its server calls the 
<b>GetConvertStg</b> function to retrieve the value of the convert bit from the storage object. If the bit is set, the object's CLSID has been changed, and the server must read the old format and write the new format for the storage object.

After retrieving the bit value, the object application should clear the convert bit by calling the 
<a href="/windows/desktop/api/ole2/nf-ole2-setconvertstg">SetConvertStg</a> function with its <i>fConvert</i> parameter set to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-setconvertstg">SetConvertStg</a>