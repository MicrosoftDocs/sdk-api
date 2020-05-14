---
UID: NF:bdatif.IEnumGuideDataProperties.Next
title: IEnumGuideDataProperties::Next (bdatif.h)
description: The Next method retrieves the specified number of items in the enumeration sequence.helpviewer_keywords: ["IEnumGuideDataProperties interface [Microsoft TV Technologies]","Next method","IEnumGuideDataProperties.Next","IEnumGuideDataProperties::Next","IEnumGuideDataPropertiesNext","Next","Next method [Microsoft TV Technologies]","Next method [Microsoft TV Technologies]","IEnumGuideDataProperties interface","bdatif/IEnumGuideDataProperties::Next","mstv.ienumguidedataproperties_next"]
old-location: mstv\ienumguidedataproperties_next.htm
tech.root: mstv
ms.assetid: 5d13ce97-5729-48e5-a742-0689b2aae1f3
ms.date: 12/05/2018
ms.keywords: IEnumGuideDataProperties interface [Microsoft TV Technologies],Next method, IEnumGuideDataProperties.Next, IEnumGuideDataProperties::Next, IEnumGuideDataPropertiesNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumGuideDataProperties interface, bdatif/IEnumGuideDataProperties::Next, mstv.ienumguidedataproperties_next
f1_keywords:
- bdatif/IEnumGuideDataProperties.Next
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdatif.h
api_name:
- IEnumGuideDataProperties.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumGuideDataProperties::Next


## -description



The <b>Next</b> method retrieves the specified number of items in the enumeration sequence.




## -parameters




### -param celt [in]

Specifies the number of items to retrieve.


### -param ppprop [out]

Address of an array of size <i>celt</i>, allocated by the caller. The array is filled with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nn-bdatif-iguidedataproperty">IGuideDataProperty</a> interface pointers.


### -param pcelt [out]

Receives the number of items received.


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The collection is at the end of the enumeration sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ienumguidedataproperties">IEnumGuideDataProperties Interface</a>
 

 

