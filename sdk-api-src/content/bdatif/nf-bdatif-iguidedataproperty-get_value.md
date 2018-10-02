---
UID: NF:bdatif.IGuideDataProperty.get_Value
title: IGuideDataProperty::get_Value
author: windows-sdk-content
description: The get_Value method retrieves the value associated with the property.
old-location: mstv\iguidedataproperty_get_value.htm
tech.root: MSTV
ms.assetid: 3a6014aa-a8a2-4436-b7a3-d083f2f0fa98
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGuideDataProperty interface [Microsoft TV Technologies],get_Value method, IGuideDataProperty.get_Value, IGuideDataProperty::get_Value, IGuideDataPropertyget_Value, bdatif/IGuideDataProperty::get_Value, get_Value, get_Value method [Microsoft TV Technologies], get_Value method [Microsoft TV Technologies],IGuideDataProperty interface, mstv.iguidedataproperty_get_value
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IGuideDataProperty.get_Value
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGuideDataProperty::get_Value


## -description



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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694107(v=VS.85).aspx">IGuideDataProperty Interface</a>
 

 

