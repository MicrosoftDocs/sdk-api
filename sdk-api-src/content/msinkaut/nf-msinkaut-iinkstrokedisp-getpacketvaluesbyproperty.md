---
UID: NF:msinkaut.IInkStrokeDisp.GetPacketValuesByProperty
title: IInkStrokeDisp::GetPacketValuesByProperty method
author: windows-driver-content
description: Retrieves the data for a known packet property from one or more packets in the stroke.
old-location: tablet\iinkstrokedisp_getpacketvaluesbyproperty.htm
old-project: tablet
ms.assetid: 135dcd06-f533-4470-b5b0-ea559c20e3c4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: 135dcd06-f533-4470-b5b0-ea559c20e3c4, GetPacketValuesByProperty method [Tablet PC], GetPacketValuesByProperty method [Tablet PC], IInkStrokeDisp interface, GetPacketValuesByProperty,IInkStrokeDisp.GetPacketValuesByProperty, IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], GetPacketValuesByProperty method, IInkStrokeDisp::GetPacketValuesByProperty, msinkaut/IInkStrokeDisp::GetPacketValuesByProperty, tablet.iinkstrokedisp_getpacketvaluesbyproperty
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.GetPacketValuesByProperty
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::GetPacketValuesByProperty method


## -description



Retrieves the data for a known packet property from one or more packets in the stroke.




## -parameters




### -param PropertyName [in]

The identifier from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants that was used to select which packet data is retrieved.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param Index [in, optional]

Optional. The starting point of the zero-based index to a packet within the stroke. The default value ISC_FirstElement, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies the first packet.


### -param Count [in, optional]

Optional. The number of points that make up the stroke data. The default value ISC_AllElements, defined in the <a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants</a> enumeration type, specifies all of the points that make up the stroke data.


### -param PacketValues [out, retval]

When this method returns, contains an array of signed 32-bit integers that specifies the value of the requested <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> for each point requested from the stroke.

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



A specific packet property may not be available on a particular <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object. A Tablet PC may have more than one tablet for user input. The <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection contains a list of all the tablets attached to the Tablet PC. Use the <a href="https://msdn.microsoft.com/4bf2e2b0-d45a-4392-990e-5e9320333c0b">IsPacketPropertySupported</a> method to determine if a particular packet property is supported by a specific <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object or by all the available tablets. Also, use the <a href="https://msdn.microsoft.com/320cc215-e4e5-4196-8e1b-ca0a30d01d37">DesiredPacketDescription</a> property of the <b>ink collector</b> to control which packet properties are collected on new strokes.




## -see-also




<b>DesiredPacketDescription Property</b>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>



<b>IsPacketPropertySupported Method</b>



<a href="https://msdn.microsoft.com/785b5ac7-b629-4948-a8bf-e92b74dacdb7">ItemSelectionConstants Enumeration</a>



<a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketPropertyGuids Constants</a>
 

 

