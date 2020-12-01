---
UID: NF:ole2.OleCreateLink
title: OleCreateLink function (ole2.h)
description: Creates an OLE compound-document linked object.
helpviewer_keywords: ["OleCreateLink","OleCreateLink function [COM]","_ole_OleCreateLink","com.olecreatelink","ole2/OleCreateLink"]
old-location: com\olecreatelink.htm
tech.root: com
ms.assetid: ef52dc37-aa63-47f3-a04f-f9d22178690f
ms.date: 12/05/2018
ms.keywords: OleCreateLink, OleCreateLink function [COM], _ole_OleCreateLink, com.olecreatelink, ole2/OleCreateLink
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
 - OleCreateLink
 - ole2/OleCreateLink
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
 - OleCreateLink
---

# OleCreateLink function


## -description

Creates an OLE compound-document linked object.

## -parameters

### -param pmkLinkSrc [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> interface on the moniker that can be used to locate the source of the linked object.

### -param riid [in]

Reference to the identifier of the interface the caller later uses to communicate with the new object (usually IID_IOleObject, defined in the OLE headers as the interface identifier for <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>).

### -param renderopt [in]

Specifies a value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. Additional considerations are described in the Remarks section below.

### -param lpFormatEtc [in]

Pointer to a value from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olerender">OLERENDER</a> that indicates the locally cached drawing or data-retrieval capabilities the newly created object is to have. The <b>OLERENDER</b> value chosen affects the possible values for the <i>lpFormatEtc</i> parameter.

### -param pClientSite [in]

Pointer to an instance of <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a>, the primary interface through which the object will request services from its container. This parameter can be <b>NULL</b>.

### -param pStg [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface on the storage object. This parameter cannot be <b>NULL</b>.

### -param ppvObj [out]

Address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly created object.

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
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Not able to bind to source.

</td>
</tr>
</table>

## -remarks

Call <b>OleCreateLink</b> to allow a container to create a link to an object.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">IOleClientSite::GetMoniker</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setmoniker">IOleObject::SetMoniker</a>