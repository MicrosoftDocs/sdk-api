---
UID: NF:bdatif.IGuideDataProperty.get_Value
title: IGuideDataProperty::get_Value (bdatif.h)
description: The get_Value method retrieves the value associated with the property.
helpviewer_keywords: ["IGuideDataProperty interface [Microsoft TV Technologies]","get_Value method","IGuideDataProperty.get_Value","IGuideDataProperty::get_Value","IGuideDataPropertyget_Value","bdatif/IGuideDataProperty::get_Value","get_Value","get_Value method [Microsoft TV Technologies]","get_Value method [Microsoft TV Technologies]","IGuideDataProperty interface","mstv.iguidedataproperty_get_value"]
old-location: mstv\iguidedataproperty_get_value.htm
tech.root: mstv
ms.assetid: 3a6014aa-a8a2-4436-b7a3-d083f2f0fa98
ms.date: 12/05/2018
ms.keywords: IGuideDataProperty interface [Microsoft TV Technologies],get_Value method, IGuideDataProperty.get_Value, IGuideDataProperty::get_Value, IGuideDataPropertyget_Value, bdatif/IGuideDataProperty::get_Value, get_Value, get_Value method [Microsoft TV Technologies], get_Value method [Microsoft TV Technologies],IGuideDataProperty interface, mstv.iguidedataproperty_get_value
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
 - IGuideDataProperty::get_Value
 - bdatif/IGuideDataProperty::get_Value
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
 - IGuideDataProperty.get_Value
---

# IGuideDataProperty::get_Value


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Value</b> method retrieves the value associated with the property.

## -parameters

### -param pvar [out]

Pointer to a variable that receives the value of the property as a <b>VARIANT</b>.

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

## -remarks

If the name of the property is "Description.Name" then the value of the property is the actual name of the service or show.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataproperty">IGuideDataProperty Interface</a>