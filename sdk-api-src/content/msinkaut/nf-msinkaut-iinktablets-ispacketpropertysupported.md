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

# IInkTablets::IsPacketPropertySupported


## -description



Determines whether a property of a tablet device or a collection of tablet devices, identified with a globally unique identifier (GUID), is supported. For example, use this method to determine if all of the tablets in a collection support tangential pressure from a pen.




## -parameters




### -param packetPropertyName [in]

The GUID for the <a href="https://msdn.microsoft.com/d3e94b57-3078-4a84-b58a-faa31bdff79e">PacketProperty GUIDs</a> of the tablet or tablets that is requested. Use a defined BSTR constant from the <a href="https://msdn.microsoft.com/3e8495f6-0860-4ea8-a258-784eaade85c7">PacketProperty</a> constants.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param Supported [out, retval]

When this method returns, contains <b>VARIANT_TRUE</b> if a known property is supported by the tablet or tablets; otherwise, <b>VARIANT_FALSE</b>.

<div class="alert"><b>Note</b>  This method can be re-entered when called within certain message handlers, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: WM_ACTIVATE, WM_ACTIVATEAPP, WM_NCACTIVATE, WM_PAINT; WM_SYSCOMMAND if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and WM_SYSKEYDOWN (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>

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



<div class="alert"><b>Note</b>  When this method is called on the <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection, it queries all of the tablets on the system. If any of them does not support the property, it returns <b>VARIANT_FALSE</b>. Call <a href="https://msdn.microsoft.com/4bf2e2b0-d45a-4392-990e-5e9320333c0b">IsPacketPropertySupported</a> on an individual <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to determine whether the device supports a known property.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/015ca2ca-3bcc-443c-a38c-7f67b69c5907">GetPacketData Method</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Class</a>



<a href="tablet.iinktablets">IInkTablets</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>



<a href="https://msdn.microsoft.com/9d90e93e-4c4a-43bd-a431-59522e332f2a">SetPacketValuesByProperty Method</a>
 

 

