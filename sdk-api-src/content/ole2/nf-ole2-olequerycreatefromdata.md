---
UID: NF:ole2.OleQueryCreateFromData
title: OleQueryCreateFromData function (ole2.h)
description: Checks whether a data object has one of the formats that would allow it to become an embedded object through a call to either the OleCreateFromData or OleCreateStaticFromData function.
helpviewer_keywords: ["OleQueryCreateFromData","OleQueryCreateFromData function [COM]","_ole_OleQueryCreateFromData","com.olequerycreatefromdata","ole2/OleQueryCreateFromData"]
old-location: com\olequerycreatefromdata.htm
tech.root: com
ms.assetid: 58fffb8c-9726-4801-84ce-6fb670b865c8
ms.date: 12/05/2018
ms.keywords: OleQueryCreateFromData, OleQueryCreateFromData function [COM], _ole_OleQueryCreateFromData, com.olequerycreatefromdata, ole2/OleQueryCreateFromData
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
 - OleQueryCreateFromData
 - ole2/OleQueryCreateFromData
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
 - Ole32.dll
 - Ext-MS-Win-Com-OLE32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - OleQueryCreateFromData
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# OleQueryCreateFromData function


## -description

Checks whether a data object has one of the formats that would allow it to become an embedded object through a call to either the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> or <a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a> function.

## -parameters

### -param pSrcDataObject [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data transfer object to be queried.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No formats are present that support either embedded- or static-object creation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_S_STATIC</b></dt>
</dl>
</td>
<td width="60%">
Formats that support static-object creation are present.

</td>
</tr>
</table>

## -remarks

When an application retrieves a data transfer object through a call to the <a href="/windows/desktop/api/ole2/nf-ole2-olegetclipboard">OleGetClipboard</a> function, the application should call <b>OleQueryCreateFromData</b> as part of the process of deciding to enable or disable the <b>Edit/Paste</b> or <b>Edit/Paste Special...</b> commands. It tests for the presence of the following formats in the data object:

<ul>
<li>CF_EMBEDDEDOBJECT</li>
<li>CF_EMBEDSOURCE</li>
<li>cfFileName</li>
<li>CF_METAFILEPICT</li>
<li>CF_DIB</li>
<li>CF_BITMAP</li>
<li>CF_ENHMETAFILE</li>
</ul>
Determining that the data object has one of these formats does not absolutely guarantee that the object creation will succeed, but is intended to help the process.

If <b>OleQueryCreateFromData</b> finds one of the CF_METAFILEPICT, CF_BITMAP,  CF_DIB, or CF_ENHMETAFILE formats and none of the other formats, it returns OLE_S_STATIC, indicating that you should call the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a> function to create the embedded object.

If <b>OleQueryCreateFromData</b> finds one of the other formats (CF_EMBEDDEDOBJECT, CF_EMBEDSOURCE, or cfFileName), even in combination with the static formats, it returns S_OK, indicating that you should call the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> function to create the embedded object.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatestaticfromdata">OleCreateStaticFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olequerylinkfromdata">OleQueryLinkFromData</a>
