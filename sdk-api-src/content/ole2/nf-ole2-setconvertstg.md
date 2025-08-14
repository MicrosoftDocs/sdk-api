---
UID: NF:ole2.SetConvertStg
title: SetConvertStg function (ole2.h)
description: The SetConvertStg function sets the convert bit in a storage object to indicate that the object is to be converted to a new class when it is opened. The setting can be retrieved with a call to the GetConvertStg function.
helpviewer_keywords: ["SetConvertStg","SetConvertStg function [Structured Storage]","_stg_setconvertstg","ole2/SetConvertStg","stg.setconvertstg"]
old-location: stg\setconvertstg.htm
tech.root: Stg
ms.assetid: 98c8fd20-6384-4656-941c-1f24d9a4d4a9
ms.date: 12/05/2018
ms.keywords: SetConvertStg, SetConvertStg function [Structured Storage], _stg_setconvertstg, ole2/SetConvertStg, stg.setconvertstg
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
 - SetConvertStg
 - ole2/SetConvertStg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - ext-ms-win-com-ole32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-1.dll
 - ext-ms-win-com-ole32-l1-1-0.dll
 - Ole32.dll
api_name:
 - SetConvertStg
---

# SetConvertStg function


## -description

The 
<b>SetConvertStg</b> function sets the convert bit in a storage object to indicate that the object is to be converted to a new class when it is opened. The setting can be retrieved with a call to the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-getconvertstg">GetConvertStg</a> function.

## -parameters

### -param pStg

<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the storage object in which to set the conversion bit.

### -param fConvert

If <b>TRUE</b>, sets the conversion bit for the object to indicate the object is to be converted when opened. If <b>FALSE</b>, clears the conversion bit.

## -returns

See the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">IStorage::CreateStream</a>, 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstream">IStorage::OpenStream</a>, 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a>, and 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> methods for possible storage and stream access errors.

## -remarks

The 
<b>SetConvertStg</b> function determines the status of the convert bit in a contained object. It is called by both the container application and the server in the process of converting an object from one class to another. When a user specifies through a <b>Convert To</b> dialog (which the container produces with a call to the 
<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuiconverta">OleUIConvert</a> function) that an object is to be converted, the container must take the following steps:

<ol>
<li>Unload the object if it is currently loaded.</li>
<li>Call 
<a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstg">WriteClassStg</a> to write the new CLSID to the object storage.</li>
<li>Call 
<a href="/windows/desktop/api/ole2/nf-ole2-writefmtusertypestg">WriteFmtUserTypeStg</a> to write the new user-type name and the existing main format to the storage.</li>
<li>Call 
<b>SetConvertStg</b> with the <i>fConvert</i> parameter set to <b>TRUE</b> to indicate that the object has been tagged for conversion to a new class the next time it is loaded.</li>
<li>Just before the object is loaded, call 
<a href="/windows/desktop/api/ole2/nf-ole2-oledoautoconvert">OleDoAutoConvert</a> to handle any needed object conversion, unless you call 
<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>, which calls it internally.</li>
</ol>
When an object is initialized from a storage object and the server is the destination of a convert-to operation, the object server should do the following:

<ol>
<li>Call the 
<a href="/windows/desktop/api/coml2api/nf-coml2api-getconvertstg">GetConvertStg</a> function to retrieve the value of the conversion bit.</li>
<li>If the bit is set, the server reads the data out of the object according to the format associated with the new CLSID.</li>
<li>When the object is asked to save itself, the object should call the 
<a href="/windows/desktop/api/ole2/nf-ole2-writefmtusertypestg">WriteFmtUserTypeStg</a> function using the normal native format and user type of the object.</li>
<li>The object should then call 
<b>SetConvertStg</b> with the <i>fConvert</i> parameter set to <b>FALSE</b> to reset the object's conversion bit.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/coml2api/nf-coml2api-getconvertstg">GetConvertStg</a>