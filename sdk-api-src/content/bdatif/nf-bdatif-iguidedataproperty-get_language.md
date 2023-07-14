---
UID: NF:bdatif.IGuideDataProperty.get_Language
title: IGuideDataProperty::get_Language (bdatif.h)
description: The get_Language method retrieves the language associated with the property.
helpviewer_keywords: ["IGuideDataProperty interface [Microsoft TV Technologies]","get_Language method","IGuideDataProperty.get_Language","IGuideDataProperty::get_Language","IGuideDataPropertyget_Language","bdatif/IGuideDataProperty::get_Language","get_Language","get_Language method [Microsoft TV Technologies]","get_Language method [Microsoft TV Technologies]","IGuideDataProperty interface","mstv.iguidedataproperty_get_language"]
old-location: mstv\iguidedataproperty_get_language.htm
tech.root: mstv
ms.assetid: e49a35f3-0517-4e84-b806-203818a0f62c
ms.date: 12/05/2018
ms.keywords: IGuideDataProperty interface [Microsoft TV Technologies],get_Language method, IGuideDataProperty.get_Language, IGuideDataProperty::get_Language, IGuideDataPropertyget_Language, bdatif/IGuideDataProperty::get_Language, get_Language, get_Language method [Microsoft TV Technologies], get_Language method [Microsoft TV Technologies],IGuideDataProperty interface, mstv.iguidedataproperty_get_language
req.header: bdatif.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGuideDataProperty::get_Language
 - bdatif/IGuideDataProperty::get_Language
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IGuideDataProperty.get_Language
---

# IGuideDataProperty::get_Language


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Language</b> method retrieves the language associated with the property.

## -parameters

### -param idLang [out]

Pointer to a variable that receives the language identifier.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataproperty">IGuideDataProperty Interface</a>