---
UID: NF:ole2.OleCreateLinkToFile
title: OleCreateLinkToFile function (ole2.h)
description: Creates an object that is linked to a file.
helpviewer_keywords: ["OleCreateLinkToFile","OleCreateLinkToFile function [COM]","_ole_OleCreateLinkToFile","com.olecreatelinktofile","ole2/OleCreateLinkToFile"]
old-location: com\olecreatelinktofile.htm
tech.root: com
ms.assetid: 06b013db-0554-4dbc-b19d-28314fb4fee0
ms.date: 12/05/2018
ms.keywords: OleCreateLinkToFile, OleCreateLinkToFile function [COM], _ole_OleCreateLinkToFile, com.olecreatelinktofile, ole2/OleCreateLinkToFile
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
 - OleCreateLinkToFile
 - ole2/OleCreateLinkToFile
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
 - OleCreateLinkToFile
---

# OleCreateLinkToFile function


## -description

Creates an object that is linked to a file.

## -parameters

### -param lpszFileName [in]

Pointer to a string naming the source file to be linked to.

### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>).

### -param renderopt [in]

Value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.

### -param lpFormatEtc [in]

Pointer to a value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.

### -param pClientSite [in]

Pointer to an instance of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.

### -param pStg [in]

 Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.

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
<dt><b>STG_E_FILENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The file name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source.

</td>
</tr>
</table>

## -remarks

The <b>OleCreateLinkToFile</b> function differs from the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a> function because it can create links both to files that are not aware of OLE, as well as to those that are using the Windows Packager.

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a>