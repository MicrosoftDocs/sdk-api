---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketValuesByProperty
title: IInkStrokeDisp::GetPacketValuesByProperty (msinkaut.h)
description: Retrieves the data for a known packet property from one or more packets in the stroke.
helpviewer_keywords: ["135dcd06-f533-4470-b5b0-ea559c20e3c4","GetPacketValuesByProperty","GetPacketValuesByProperty method [Tablet PC]","GetPacketValuesByProperty method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","GetPacketValuesByProperty method","IInkStrokeDisp.GetPacketValuesByProperty","IInkStrokeDisp::GetPacketValuesByProperty","msinkaut/IInkStrokeDisp::GetPacketValuesByProperty","tablet.iinkstrokedisp_getpacketvaluesbyproperty"]
old-location: tablet\iinkstrokedisp_getpacketvaluesbyproperty.htm
tech.root: tablet
ms.assetid: 135dcd06-f533-4470-b5b0-ea559c20e3c4
ms.date: 12/05/2018
ms.keywords: 135dcd06-f533-4470-b5b0-ea559c20e3c4, GetPacketValuesByProperty, GetPacketValuesByProperty method [Tablet PC], GetPacketValuesByProperty method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPacketValuesByProperty method, IInkStrokeDisp.GetPacketValuesByProperty, IInkStrokeDisp::GetPacketValuesByProperty, msinkaut/IInkStrokeDisp::GetPacketValuesByProperty, tablet.iinkstrokedisp_getpacketvaluesbyproperty
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
 - IInkStrokeDisp::GetPacketValuesByProperty
 - msinkaut/IInkStrokeDisp::GetPacketValuesByProperty
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
 - IInkStrokeDisp.GetPacketValuesByProperty
---

# IInkStrokeDisp::GetPacketValuesByProperty


## -description

Retrieves the data for a known packet property from one or more packets in the stroke.

## -parameters

### -param PropertyName [in]

The identifier from the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> constants that was used to select which packet data is retrieved.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Index [in, optional]

Optional. The starting point of the zero-based index to a packet within the stroke. The default value ISC_FirstElement, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies the first packet.

### -param Count [in, optional]

Optional. The number of points that make up the stroke data. The default value ISC_AllElements, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.

### -param PacketValues [out, retval]

When this method returns, contains an array of signed 32-bit integers that specifies the value of the requested <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> for each point requested from the stroke.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

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
<dt><b>TPC_E_INVALID_STROKE</b></dt>
</dl>
</td>
<td width="60%">
The stroke is invalid.

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
Cannot allocate packet data array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid index, count, or packet property.

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
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
</table>

## -remarks

A specific packet property may not be available on a particular <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object. A Tablet PC may have more than one tablet for user input. The <a href="/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets</a> collection contains a list of all the tablets attached to the Tablet PC. Use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported">IsPacketPropertySupported</a> method to determine if a particular packet property is supported by a specific <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object or by all the available tablets. Also, use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription">DesiredPacketDescription</a> property of the <b>ink collector</b> to control which packet properties are collected on new strokes.

## -see-also

<b>DesiredPacketDescription Property</b>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets Collection</a>



<b>IsPacketPropertySupported Method</b>



<a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ItemSelectionConstants Enumeration</a>



<a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>