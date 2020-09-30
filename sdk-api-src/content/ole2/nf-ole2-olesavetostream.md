---
UID: NF:ole2.OleSaveToStream
title: OleSaveToStream function (ole2.h)
description: Saves an object with the IPersistStream interface on it to the specified stream.
helpviewer_keywords: ["OleSaveToStream","OleSaveToStream function [COM]","_ole_OleSaveToStream","com.olesavetostream","ole/OleSaveToStream"]
old-location: com\olesavetostream.htm
tech.root: com
ms.assetid: 0085c6a8-1a94-4379-9937-c8d792d130da
ms.date: 12/05/2018
ms.keywords: OleSaveToStream, OleSaveToStream function [COM], _ole_OleSaveToStream, com.olesavetostream, ole/OleSaveToStream
req.header: ole2.h
req.include-header: Ole2.h
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
 - OleSaveToStream
 - ole2/OleSaveToStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleSaveToStream
---

# OleSaveToStream function


## -description

Saves an object with the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> interface on it to the specified stream.

## -parameters

### -param pPStm [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> interface on the object to be saved to the stream. The <i>pPStm</i> parameter cannot be <b>NULL</b>.

### -param pStm [in]

 Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface on the stream in which the object is to be saved.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STGMEDIUM_E_FULL</b></dt>
</dl>
</td>
<td width="60%">
The object could not be saved due to lack of disk space.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPStm</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by the <a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a> function or the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-save">IPersistStream::Save</a> method.

## -remarks

This function simplifies saving an object that implements the <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> interface to a stream. In this stream, the object's CLSID precedes its data. When the stream is retrieved, the CLSID permits the proper code to be associated with the data. The <b>OleSaveToStream</b> function does the following:

<ul>
<li>Calls the <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">IPersist::GetClassID</a> method to get the object's CLSID.</li>
<li>Writes the CLSID to the stream with the <a href="/windows/desktop/api/coml2api/nf-coml2api-writeclassstm">WriteClassStm</a> function.</li>
<li>Calls the <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-save">IPersistStream::Save</a> method with <i>fClearDirty</i> set to <b>TRUE</b>, which clears the dirty bit in the object.</li>
</ul>
The companion helper, <a href="/windows/desktop/api/ole/nf-ole-oleloadfromstream">OleLoadFromStream</a>, loads objects saved in this way.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/api/ole/nf-ole-oleloadfromstream">OleLoadFromStream</a>