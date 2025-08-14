---
UID: NF:ole2.OleCreateLinkFromData
title: OleCreateLinkFromData function (ole2.h)
description: Creates a linked object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation.
helpviewer_keywords: ["OleCreateLinkFromData","OleCreateLinkFromData function [COM]","_ole_OleCreateLinkFromData","com.olecreatelinkfromdata","ole2/OleCreateLinkFromData"]
old-location: com\olecreatelinkfromdata.htm
tech.root: com
ms.assetid: 3eda0cf5-c33d-43cf-ba8a-02a4f6383adc
ms.date: 12/05/2018
ms.keywords: OleCreateLinkFromData, OleCreateLinkFromData function [COM], _ole_OleCreateLinkFromData, com.olecreatelinkfromdata, ole2/OleCreateLinkFromData
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
 - OleCreateLinkFromData
 - ole2/OleCreateLinkFromData
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
 - OleCreateLinkFromData
---

# OleCreateLinkFromData function


## -description

Creates a linked object from a data transfer object retrieved either from the clipboard or as part of an OLE drag-and-drop operation.

## -parameters

### -param pSrcDataObj [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data transfer object from which the linked object is to be created.

### -param riid [in]

Reference to the identifier of interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>).

### -param renderopt [in]

Value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the following Remarks section.

### -param pFormatEtc [in]

 Pointer to a value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>pFormatEtc</i> parameter.

### -param pClientSite [in]

 Pointer to an instance of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.

### -param pStg [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return,   <i>ppvObj</i> contains the requested interface pointer on the newly created object.

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
<dt><b>CLIPBRD_E_CANT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
Not able to open the clipboard.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_GETMONIKER</b></dt>
</dl>
</td>
<td width="60%">
Not able to extract the object's moniker.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source. Binding is necessary to get the cache's initialization data.


</td>
</tr>
</table>

## -remarks

The <b>OleCreateLinkFromData</b> function is used to implement either a paste-link or a drag-link operation. Its operation is similar to that of the <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a> function, except that it creates a link, and looks for different data formats. If the CF_LINKSOURCE format is not present, and either the FileName or FileNameW clipboard format is present in the data transfer object, <b>OleCreateLinkFromData</b> creates a package containing the link to the indicated file.



You use the renderopt and <i>pFormatetc</i> parameters to control the caching capability of the newly created object. For general information on how to determine what is to be cached, refer to the <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> enumeration for a description of the interaction between renderopt and <i>pFormatetc</i>. There are, however, some additional specific effects of these parameters on the way <b>OleCreateLinkFromData</b> initializes the cache, as follows.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>
OLERENDER_DRAW, OLERENDER_FORMAT


</td>
<td>
If the presentation information is in the other formats in the source data object, this information is used. If the information is not present, the cache is initially empty, but will be filled the first time the object is run. No other formats are cached in the newly created object.


</td>
</tr>
<tr>
<td>
OLERENDER_NONE, OLERENDER_ASIS


</td>
<td>
Nothing is to be cached in the newly created object.


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ole2/nf-ole2-olecreatelink">OleCreateLink</a>