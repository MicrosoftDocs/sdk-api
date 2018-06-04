---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInkStrokeDisp::SetPacketValuesByProperty


## -description



          Modifies the packet values for a particular property.
        


## -parameters




### -param bstrPropertyName [in]

The globally unique identifier (GUID) identifier from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants that is used to select which packet data is set. Use <a href="https://msdn.microsoft.com/c81f14e2-d97f-42cd-8498-240f8d39f9bc">PacketDescription</a> to determine the defined properties for this stroke.


### -param PacketValues [in]

The array of packet data values. The method fails if any of the values in the array are outside the minimum or maximum value of the property. To determine the range of values in the property, call the <a href="https://msdn.microsoft.com/21b13777-d924-45d6-bdcc-284c9b7d9627">GetPacketDescriptionPropertyMetrics</a> method.


### -param Index [in, optional]

Optional. The starting index of the packet to be modified. The default value <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ISC_FirstElement</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies the first packet.


### -param Count [in, optional]

Optional. Specifies the number of packets in the stroke to modify and the number of values in <i>PacketValues</i>. The default value <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ISC_AllElements</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies that all packets are modified.


### -param NumberOfPacketsSet [out, retval]

When this method returns, contains the actual number of packets set.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid variant, index (out of range), or property GUID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21b13777-d924-45d6-bdcc-284c9b7d9627">GetPacketDescriptionPropertyMetrics Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants Enumeration</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

