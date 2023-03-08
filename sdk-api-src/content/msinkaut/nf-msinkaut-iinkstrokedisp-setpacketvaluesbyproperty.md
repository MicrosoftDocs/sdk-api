---
UID: NF:msinkaut.IInkStrokeDisp.SetPacketValuesByProperty
title: IInkStrokeDisp::SetPacketValuesByProperty (msinkaut.h)
description: Modifies the packet values for a particular property.
helpviewer_keywords: ["9d90e93e-4c4a-43bd-a431-59522e332f2a","IInkStrokeDisp interface [Tablet PC]","SetPacketValuesByProperty method","IInkStrokeDisp.SetPacketValuesByProperty","IInkStrokeDisp::SetPacketValuesByProperty","SetPacketValuesByProperty","SetPacketValuesByProperty method [Tablet PC]","SetPacketValuesByProperty method [Tablet PC]","IInkStrokeDisp interface","msinkaut/IInkStrokeDisp::SetPacketValuesByProperty","tablet.iinkstrokedisp_setpacketvaluesbyproperty"]
old-location: tablet\iinkstrokedisp_setpacketvaluesbyproperty.htm
tech.root: tablet
ms.assetid: 9d90e93e-4c4a-43bd-a431-59522e332f2a
ms.date: 12/05/2018
ms.keywords: 9d90e93e-4c4a-43bd-a431-59522e332f2a, IInkStrokeDisp interface [Tablet PC],SetPacketValuesByProperty method, IInkStrokeDisp.SetPacketValuesByProperty, IInkStrokeDisp::SetPacketValuesByProperty, SetPacketValuesByProperty, SetPacketValuesByProperty method [Tablet PC], SetPacketValuesByProperty method [Tablet PC],IInkStrokeDisp interface, msinkaut/IInkStrokeDisp::SetPacketValuesByProperty, tablet.iinkstrokedisp_setpacketvaluesbyproperty
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
 - IInkStrokeDisp::SetPacketValuesByProperty
 - msinkaut/IInkStrokeDisp::SetPacketValuesByProperty
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
 - IInkStrokeDisp.SetPacketValuesByProperty
---

# IInkStrokeDisp::SetPacketValuesByProperty


## -description

Modifies the packet values for a particular property.

## -parameters

### -param bstrPropertyName [in]

The globally unique identifier (GUID) identifier from the <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> constants that is used to select which packet data is set. Use <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription">PacketDescription</a> to determine the defined properties for this stroke.

### -param PacketValues [in]

The array of packet data values. The method fails if any of the values in the array are outside the minimum or maximum value of the property. To determine the range of values in the property, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics</a> method.

### -param Index [in, optional]

Optional. The starting index of the packet to be modified. The default value <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ISC_FirstElement</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies the first packet.

### -param Count [in, optional]

Optional. Specifies the number of packets in the stroke to modify and the number of values in <i>PacketValues</i>. The default value <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ISC_AllElements</a>, defined in the <b>ItemSelectionConstants</b> enumeration type, specifies that all packets are modified.

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

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ItemSelectionConstants Enumeration</a>



<a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketPropertyGuids Constants</a>