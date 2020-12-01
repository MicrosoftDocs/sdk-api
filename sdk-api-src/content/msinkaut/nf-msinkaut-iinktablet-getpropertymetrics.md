---
UID: NF:msinkaut.IInkTablet.GetPropertyMetrics
title: IInkTablet::GetPropertyMetrics (msinkaut.h)
description: Retrieves the metrics data for a specified property.
helpviewer_keywords: ["9656bb56-01aa-4e9b-a3ad-4fbf117cdfeb","GetPropertyMetrics","GetPropertyMetrics method [Tablet PC]","GetPropertyMetrics method [Tablet PC]","IInkTablet interface","IInkTablet interface [Tablet PC]","GetPropertyMetrics method","IInkTablet.GetPropertyMetrics","IInkTablet::GetPropertyMetrics","msinkaut/IInkTablet::GetPropertyMetrics","tablet.iinktablet_getpropertymetrics"]
old-location: tablet\iinktablet_getpropertymetrics.htm
tech.root: tablet
ms.assetid: 9656bb56-01aa-4e9b-a3ad-4fbf117cdfeb
ms.date: 12/05/2018
ms.keywords: 9656bb56-01aa-4e9b-a3ad-4fbf117cdfeb, GetPropertyMetrics, GetPropertyMetrics method [Tablet PC], GetPropertyMetrics method [Tablet PC],IInkTablet interface, IInkTablet interface [Tablet PC],GetPropertyMetrics method, IInkTablet.GetPropertyMetrics, IInkTablet::GetPropertyMetrics, msinkaut/IInkTablet::GetPropertyMetrics, tablet.iinktablet_getpropertymetrics
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
 - IInkTablet::GetPropertyMetrics
 - msinkaut/IInkTablet::GetPropertyMetrics
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
 - IInkTablet.GetPropertyMetrics
---

# IInkTablet::GetPropertyMetrics


## -description

Retrieves the metrics data for a specified property.

## -parameters

### -param propertyName [in]

The property for which you want to determine metrics.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Minimum [out]

The minimum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 has a logical minimum of 0.

### -param Maximum [out]

The maximum value, in logical units, that the tablet reports for this property. For example, a tablet reporting x-values from 0 to 9000 would have a logical maximum of 9000.

### -param Units [out]

The physical units of the property, such as inches or degrees. For a list of property units, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit">TabletPropertyMetricUnit</a> enumeration type.

### -param Resolution [out]

Specifies the resolution or increment value for the <b>units</b> member. For example, a tablet that reports 400 dots per inch (dpi) has a  resolution value of 400.

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
<dt><b>TPC_E_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The tablet does not support the specified property.

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
Unknown property string.

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

## -remarks

The properties for which you retrieve metrics may include the time that a packet was generated or the downward pressure of the pen tip on the tablet surface.

For a complete list of properties for which you can retrieve metrics, see the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> constants.

<div class="alert"><b>Note</b>  Accessing this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WMNCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <b>wParam</b> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty">GetPacketValuesByProperty Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty">SetPacketValuesByProperty Method</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit">TabletPropertyMetricUnit Enumeration</a>