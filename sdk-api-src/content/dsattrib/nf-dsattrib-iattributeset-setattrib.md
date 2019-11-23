---
UID: NF:dsattrib.IAttributeSet.SetAttrib
title: IAttributeSet::SetAttrib (dsattrib.h)

description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iattributeset_setattrib.htm
tech.root: mstv
ms.assetid: 5f2dc759-5545-4b4a-a2fc-fca65c0856cd

ms.date: 12/05/2018
ms.keywords: IAttributeSet interface [Microsoft TV Technologies],SetAttrib method, IAttributeSet.SetAttrib, IAttributeSet::SetAttrib, IAttributeSetSetAttrib, SetAttrib, SetAttrib method [Microsoft TV Technologies], SetAttrib method [Microsoft TV Technologies],IAttributeSet interface, dsattrib/IAttributeSet::SetAttrib, mstv.iattributeset_setattrib
ms.topic: method
f1_keywords: 
 - "dsattrib/IAttributeSet.SetAttrib"
dev_langs:
 - c++
req.header: dsattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dsattrib.h
api_name:
 - IAttributeSet.SetAttrib
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAttributeSet::SetAttrib


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>SetAttrib</b> method sets an attribute on the object.


## -parameters




### -param guidAttribute [in]

<b>GUID</b> that identifies the attribute.


### -param pbAttribute [in]

Pointer to a buffer that contains the attribute value.


### -param dwAttributeLength [in]

Size of the <i>pbAttribute</i> buffer, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>__HRESULT_FROM_WIN32(ERROR_DUPLICATE_TAG)</b></dt>
</dl>
</td>
<td width="60%">
An attribute with this <b>GUID</b> already exists on this object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dsattrib/nn-dsattrib-iattributeset">IAttributeSet Interface</a>
 

 

