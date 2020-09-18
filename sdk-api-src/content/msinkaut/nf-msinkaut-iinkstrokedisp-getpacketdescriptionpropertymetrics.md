---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketDescriptionPropertyMetrics
title: IInkStrokeDisp::GetPacketDescriptionPropertyMetrics (msinkaut.h)
description: Retrieves the metrics for a given packet description type.
helpviewer_keywords: ["21b13777-d924-45d6-bdcc-284c9b7d9627","GetPacketDescriptionPropertyMetrics","GetPacketDescriptionPropertyMetrics method [Tablet PC]","GetPacketDescriptionPropertyMetrics method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","GetPacketDescriptionPropertyMetrics method","IInkStrokeDisp.GetPacketDescriptionPropertyMetrics","IInkStrokeDisp::GetPacketDescriptionPropertyMetrics","msinkaut/IInkStrokeDisp::GetPacketDescriptionPropertyMetrics","tablet.iinkstrokedisp_getpacketdescriptionpropertymetrics"]
old-location: tablet\iinkstrokedisp_getpacketdescriptionpropertymetrics.htm
tech.root: tablet
ms.assetid: 21b13777-d924-45d6-bdcc-284c9b7d9627
ms.date: 12/05/2018
ms.keywords: 21b13777-d924-45d6-bdcc-284c9b7d9627, GetPacketDescriptionPropertyMetrics, GetPacketDescriptionPropertyMetrics method [Tablet PC], GetPacketDescriptionPropertyMetrics method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPacketDescriptionPropertyMetrics method, IInkStrokeDisp.GetPacketDescriptionPropertyMetrics, IInkStrokeDisp::GetPacketDescriptionPropertyMetrics, msinkaut/IInkStrokeDisp::GetPacketDescriptionPropertyMetrics, tablet.iinkstrokedisp_getpacketdescriptionpropertymetrics
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkStrokeDisp::GetPacketDescriptionPropertyMetrics
 - msinkaut/IInkStrokeDisp::GetPacketDescriptionPropertyMetrics
dev_langs:
 - c++
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
---

# IInkStrokeDisp::GetPacketDescriptionPropertyMetrics


## -description

Retrieves the metrics for a given packet description type.

## -parameters

### -param PropertyName [in]

The globally unique identifier (GUID) from the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> constants that identifies the property for which to obtain metrics.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Minimum [out]

The minimum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 would have a logical minimum of 0.

### -param Maximum [out]

The maximum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 would have a logical maximum of 9000.

### -param Units [out]

The physical units of the property, such as inches or degrees. For a list of property units, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit">TabletPropertyMetricUnit</a> enumeration type.

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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty">GetPacketValuesByProperty Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics">GetPropertyMetrics Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty">SetPacketValuesByProperty Method</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit">TabletPropertyMetricUnit Enumeration</a>