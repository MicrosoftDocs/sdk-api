---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketDescriptionPropertyMetrics
title: IInkStrokeDisp::GetPacketDescriptionPropertyMetrics
author: windows-sdk-content
description: Retrieves the metrics for a given packet description type.
old-location: tablet\iinkstrokedisp_getpacketdescriptionpropertymetrics.htm
tech.root: tablet
ms.assetid: 21b13777-d924-45d6-bdcc-284c9b7d9627
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 21b13777-d924-45d6-bdcc-284c9b7d9627, GetPacketDescriptionPropertyMetrics, GetPacketDescriptionPropertyMetrics method [Tablet PC], GetPacketDescriptionPropertyMetrics method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPacketDescriptionPropertyMetrics method, IInkStrokeDisp.GetPacketDescriptionPropertyMetrics, IInkStrokeDisp::GetPacketDescriptionPropertyMetrics, msinkaut/IInkStrokeDisp::GetPacketDescriptionPropertyMetrics, tablet.iinkstrokedisp_getpacketdescriptionpropertymetrics
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
 - IInkStrokeDisp.GetPacketDescriptionPropertyMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkStrokeDisp.GetPacketDescriptionPropertyMetrics
: 
---

# IInkStrokeDisp::GetPacketDescriptionPropertyMetrics


## -description



Retrieves the metrics for a given packet description type.




## -parameters




### -param PropertyName [in]

The globally unique identifier (GUID) from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants that identifies the property for which to obtain metrics.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param Minimum [out]

The minimum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 would have a logical minimum of 0.


### -param Maximum [out]

The maximum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 would have a logical maximum of 9000.


### -param Units [out]

The physical units of the property, such as inches or degrees. For a list of property units, see the <a href="https://msdn.microsoft.com/c2258c48-4062-4528-9ebb-21cdbecf70ab">TabletPropertyMetricUnit</a> enumeration type.


### -param Resolution [out]

The resolution or increment value for the <i>units</i> member. For example, a tablet that reports 400 dots per inch (dpi) would have a <i>resolution</i> value of 400.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory necessary to complete this request.

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
The property does not exist in the collection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/135dcd06-f533-4470-b5b0-ea559c20e3c4">GetPacketValuesByProperty Method</a>



<a href="https://msdn.microsoft.com/9656bb56-01aa-4e9b-a3ad-4fbf117cdfeb">GetPropertyMetrics Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/9d90e93e-4c4a-43bd-a431-59522e332f2a">SetPacketValuesByProperty Method</a>



<a href="https://msdn.microsoft.com/c2258c48-4062-4528-9ebb-21cdbecf70ab">TabletPropertyMetricUnit Enumeration</a>
 

 

