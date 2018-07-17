---
UID: NF:msinkaut.IInkTablet.IsPacketPropertySupported
title: IInkTablet::IsPacketPropertySupported
author: windows-sdk-content
description: Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported.
old-location: tablet\iinktablet_ispacketpropertysupported.htm
old-project: tablet
ms.assetid: 4bf2e2b0-d45a-4392-990e-5e9320333c0b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 4bf2e2b0-d45a-4392-990e-5e9320333c0b, IInkTablet interface [Tablet PC],IsPacketPropertySupported method, IInkTablet.IsPacketPropertySupported, IInkTablet::IsPacketPropertySupported, IsPacketPropertySupported, IsPacketPropertySupported method [Tablet PC], IsPacketPropertySupported method [Tablet PC],IInkTablet interface, msinkaut/IInkTablet::IsPacketPropertySupported, tablet.iinktablet_ispacketpropertysupported
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkTablet.IsPacketPropertySupported
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTablet::IsPacketPropertySupported


## -description



Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. For example, use this method to determine if all of the tablets in a collection support tangential pressure from a pen.




## -parameters




### -param packetPropertyName




### -param Supported [out, retval]

<b>VARIANT_TRUE</b> if a known property is supported by the tablet or tablets; otherwise, <b>VARIANT_FALSE</b>.

<div class="alert"><b>Note</b>  This method can be re-entered when called within certain message handlers, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WM_NCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

#### - packetProperty [in]

The GUID for the <a href="https://msdn.microsoft.com/d3e94b57-3078-4a84-b58a-faa31bdff79e">PacketProperty GUIDs</a> of the tablet or tablets that is requested. Use a defined BSTR constant from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  When this method is called on the <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection, it queries all of the tablets on the system. If any of them does not support the property, it returns <b>FALSE</b>. Call <b>IsPacketPropertySupported</b> on an individual <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to determine whether the device supports a known property.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/015ca2ca-3bcc-443c-a38c-7f67b69c5907">GetPacketData Method</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/9d90e93e-4c4a-43bd-a431-59522e332f2a">SetPacketValuesByProperty Method</a>
 

 

