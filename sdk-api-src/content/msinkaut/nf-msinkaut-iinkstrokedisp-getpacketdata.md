---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketData
title: IInkStrokeDisp::GetPacketData
author: windows-sdk-content
description: Retrieves the packet data for a range of packets within the IInkStrokeDisp object.
old-location: tablet\iinkstrokedisp_getpacketdata.htm
tech.root: tablet
ms.assetid: 015ca2ca-3bcc-443c-a38c-7f67b69c5907
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 015ca2ca-3bcc-443c-a38c-7f67b69c5907, GetPacketData, GetPacketData method [Tablet PC], GetPacketData method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPacketData method, IInkStrokeDisp.GetPacketData, IInkStrokeDisp::GetPacketData, msinkaut/IInkStrokeDisp::GetPacketData, tablet.iinkstrokedisp_getpacketdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokeDisp.GetPacketData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkStrokeDisp::GetPacketData


## -description



Retrieves the packet data for a range of packets within the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.




## -parameters




### -param Index [in, optional]

Optional. The starting point of the zero-based index to a packet within the stroke. The default value ISC_FirstElement, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies the first packet.


### -param Count [in, optional]

Optional. The number of point packet data sets that should be returned, starting with the packet specified in the <i>startingIndex</i> parameter. The default value ISC_AllElements, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.


### -param PacketData [out, retval]

When this method returns, contains a signed 32-bit integer array containing the packet data for the requested points in the stroke. The array contains the data for the first point, then the data for the second point, and so on.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate Stroke handler helper object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The stroke is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -remarks



If the number of packets in the stroke is less than the sum of the <i>startingIndex</i> and <i>pointCount</i> parameters, then the returned array of data contains packet information for fewer points than the count requested.

To retrieve the description of the packet data, use the stroke's <a href="https://msdn.microsoft.com/c81f14e2-d97f-42cd-8498-240f8d39f9bc">PacketDescription</a> property. This property returns an array of globally unique identifier (GUID) that indicates which property values are returned by the <b>GetPacketData</b> method for each point. The <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants contain the available packet property GUIDs.




## -see-also




<a href="https://msdn.microsoft.com/21b13777-d924-45d6-bdcc-284c9b7d9627">GetPacketDescriptionPropertyMetrics Method</a>



<a href="https://msdn.microsoft.com/135dcd06-f533-4470-b5b0-ea559c20e3c4">GetPacketValuesByProperty Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants Enumeration</a>



<a href="https://msdn.microsoft.com/f7cd47f8-809b-455d-873f-81dba80549b9">PacketCount Property</a>



<a href="https://msdn.microsoft.com/c81f14e2-d97f-42cd-8498-240f8d39f9bc">PacketDescription Property</a>



<a href="https://msdn.microsoft.com/42016aa0-7cc4-43d5-a055-7007a4bf9f07">PacketSize Property</a>



<a href="https://msdn.microsoft.com/9d90e93e-4c4a-43bd-a431-59522e332f2a">SetPacketValuesByProperty Method</a>
 

 

