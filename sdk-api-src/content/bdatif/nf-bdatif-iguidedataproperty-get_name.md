---
UID: NF:bdatif.IGuideDataProperty.get_Name
title: IGuideDataProperty::get_Name method
author: windows-driver-content
description: The get_Name method retrieves the name of the property.
old-location: mstv\iguidedataproperty_get_name.htm
old-project: mstv
ms.assetid: 63606e76-fd4a-4954-93bd-1085d32dd2da
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IGuideDataProperty, IGuideDataProperty interface [Microsoft TV Technologies], get_Name method, IGuideDataProperty::get_Name, IGuideDataPropertyget_Name, bdatif/IGuideDataProperty::get_Name, get_Name method [Microsoft TV Technologies], get_Name method [Microsoft TV Technologies], IGuideDataProperty interface, get_Name,IGuideDataProperty.get_Name, mstv.iguidedataproperty_get_name
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
req.typenames: SpanningEventEmmMessage
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdatif.h
api_name:
-	IGuideDataProperty.get_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGuideDataProperty::get_Name method


## -description



The <b>get_Name</b> method retrieves the name of the property.




## -parameters




### -param pbstrName [out]

Pointer to a variable that receives a string containing the property name, for example "Description.ID" or "Description.Title".


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c614f2a-69e0-4100-b83e-740478654c17">IGuideDataProperty Interface</a>
 

 

