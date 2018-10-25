---
UID: NF:recapis.AddStroke
title: AddStroke function
author: windows-sdk-content
description: Adds an ink stroke to the RecognizerContext.
old-location: tablet\addstroke.htm
tech.root: tablet
ms.assetid: 1db3dbef-41bf-4b00-8e6c-07c7c414e595
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 1db3dbef-41bf-4b00-8e6c-07c7c414e595, AddStroke, AddStroke function [Tablet PC], recapis/AddStroke, tablet.addstroke
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - AddStroke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddStroke function


## -description



Adds an ink stroke to the <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">RecognizerContext</a>.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param pPacketDesc

Describes the contents of the packets. The description must match the contents of the packets in <i>pPacket</i>. If <b>NULL</b>, this function uses the <a href="https://msdn.microsoft.com/6600b345-db7a-49ca-a54a-7d212952cb8f">GetPreferredPacketDescription</a> function.


### -param cbPacket

Size, in bytes, of the <i>pPacket</i> buffer.


### -param pPacket

Array of packets that contain tablet space coordinates.


### -param pXForm

Describes the transform that can be applied to ink to transform it from tablet space into ink space. A recognizer may choose to ignore this transform and implement their own ink rotation algorithms. These recognizers should still return properties calculated in the lattice data relative to this transform.


## -returns



This function can return one of these values.

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
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_PACKET_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
The packet description does not contain the necessary information for the packet to be considered valid. For example, it does not include a GUID_X or GUID_Y property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_OUT_OF_ORDER_CALL</b></dt>
</dl>
</td>
<td width="60%">
The call to the method was made out of order.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -remarks



The recognizer must return properties such as <a href="https://msdn.microsoft.com/5fb53534-b15f-44e8-8bb3-31d6ba3a9bb4">Baseline</a> in ink space coordinates rather than tablet coordinates.

It is recommended that your recognizer place a limit on the number of strokes per context and/or the points allowed in a given stroke. Limit input to 1024 strokes per context and 32767 points per stroke.

Strokes with zero points are not allowed. You should return E_FAIL in such a case.




## -see-also




<a href="https://msdn.microsoft.com/6600b345-db7a-49ca-a54a-7d212952cb8f">GetPreferredPacketDescription</a>



<a href="https://msdn.microsoft.com/6823f2c6-2c99-4b9a-8208-041fc1f7bf82">PACKET_DESCRIPTION Structure</a>
 

 

