---
UID: NF:objidlbase.IMarshalingStream.GetMarshalingContextAttribute
title: IMarshalingStream::GetMarshalingContextAttribute (objidlbase.h)
description: The IMarshalingStream::GetMarshalingContextAttribute (objidlbase.h) method gets information about the marshaling context.
helpviewer_keywords: ["GetMarshalingContextAttribute","GetMarshalingContextAttribute method [COM]","GetMarshalingContextAttribute method [COM]","IMarshalingStream interface","IMarshalingStream interface [COM]","GetMarshalingContextAttribute method","IMarshalingStream.GetMarshalingContextAttribute","IMarshalingStream::GetMarshalingContextAttribute","com.imarshalingstream_getmarshalingcontextattribute","objidl/IMarshalingStream::GetMarshalingContextAttribute"]
old-location: com\imarshalingstream_getmarshalingcontextattribute.htm
tech.root: com
ms.assetid: 60B401C8-1ACA-412D-B754-997C39454821
ms.date: 08/13/2022
ms.keywords: GetMarshalingContextAttribute, GetMarshalingContextAttribute method [COM], GetMarshalingContextAttribute method [COM],IMarshalingStream interface, IMarshalingStream interface [COM],GetMarshalingContextAttribute method, IMarshalingStream.GetMarshalingContextAttribute, IMarshalingStream::GetMarshalingContextAttribute, com.imarshalingstream_getmarshalingcontextattribute, objidl/IMarshalingStream::GetMarshalingContextAttribute
req.header: objidlbase.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMarshalingStream::GetMarshalingContextAttribute
 - objidlbase/IMarshalingStream::GetMarshalingContextAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IMarshalingStream.GetMarshalingContextAttribute
---

# IMarshalingStream::GetMarshalingContextAttribute


## -description

Gets information about the marshaling context.

## -parameters

### -param attribute [in]

The attribute to query.

### -param pAttributeValue [out]

The value of <i>attribute</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each possible value of the attribute parameter is paired with the data type of the attribute this identifies.

You can query the following attributes with this method.

<table>
<tr>
<th>Attribute</th>
<th>Values</th>
</tr>
<tr>
<td>
CO_MARSHALING_SOURCE_IS_APP_CONTAINER

</td>
<td>
This attribute is a boolean value, with 0 representing <b>TRUE</b> and nonzero representing <b>FALSE</b>. You can safely cast the value of the result to <b>BOOL</b>, but it isn't safe for the caller to cast a <b>BOOL*</b> to <b>ULONG_PTR*</b> for the <i>pAttributeValue</i> parameter, or for the implementation to cast <i>pAttributeValue</i> to <b>BOOL*</b> when setting it.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/ne-objidl-co_marshaling_context_attributes">CO_MARSHALING_CONTEXT_ATTRIBUTES</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iglobaloptions">IGlobalOptions</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshalingstream">IMarshalingStream</a>
