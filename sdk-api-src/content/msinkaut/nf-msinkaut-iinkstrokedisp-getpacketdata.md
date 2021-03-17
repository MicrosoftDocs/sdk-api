---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketData
title: IInkStrokeDisp::GetPacketData (msinkaut.h)
description: Retrieves the packet data for a range of packets within the IInkStrokeDisp object.
helpviewer_keywords: ["015ca2ca-3bcc-443c-a38c-7f67b69c5907","GetPacketData","GetPacketData method [Tablet PC]","GetPacketData method [Tablet PC]","IInkStrokeDisp interface","IInkStrokeDisp interface [Tablet PC]","GetPacketData method","IInkStrokeDisp.GetPacketData","IInkStrokeDisp::GetPacketData","msinkaut/IInkStrokeDisp::GetPacketData","tablet.iinkstrokedisp_getpacketdata"]
old-location: tablet\iinkstrokedisp_getpacketdata.htm
tech.root: tablet
ms.assetid: 015ca2ca-3bcc-443c-a38c-7f67b69c5907
ms.date: 12/05/2018
ms.keywords: 015ca2ca-3bcc-443c-a38c-7f67b69c5907, GetPacketData, GetPacketData method [Tablet PC], GetPacketData method [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],GetPacketData method, IInkStrokeDisp.GetPacketData, IInkStrokeDisp::GetPacketData, msinkaut/IInkStrokeDisp::GetPacketData, tablet.iinkstrokedisp_getpacketdata
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
 - IInkStrokeDisp::GetPacketData
 - msinkaut/IInkStrokeDisp::GetPacketData
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
 - IInkStrokeDisp.GetPacketData
---

# IInkStrokeDisp::GetPacketData


## -description

Retrieves the packet data for a range of packets within the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object.

## -parameters

### -param Index [in, optional]

Optional. The starting point of the zero-based index to a packet within the stroke. The default value ISC_FirstElement, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies the first packet.

### -param Count [in, optional]

Optional. The number of point packet data sets that should be returned, starting with the packet specified in the <i>startingIndex</i> parameter. The default value ISC_AllElements, defined in the <a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">InkSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.

### -param PacketData [out, retval]

When this method returns, contains a signed 32-bit integer array containing the packet data for the requested points in the stroke. The array contains the data for the first point, then the data for the second point, and so on.

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

To retrieve the description of the packet data, use the stroke's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription">PacketDescription</a> property. This property returns an array of globally unique identifier (GUID) that indicates which property values are returned by the <b>GetPacketData</b> method for each point. The <a href="/windows/desktop/tablet/packetpropertyguids-constants">PacketProperty</a> constants contain the available packet property GUIDs.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketdescriptionpropertymetrics">GetPacketDescriptionPropertyMetrics Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getpacketvaluesbyproperty">GetPacketValuesByProperty Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp Interface</a>



<a href="/windows/win32/api/msinkaut/ne-msinkaut-inkselectionconstants">ItemSelectionConstants Enumeration</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetcount">PacketCount Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription">PacketDescription Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetsize">PacketSize Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-setpacketvaluesbyproperty">SetPacketValuesByProperty Method</a>