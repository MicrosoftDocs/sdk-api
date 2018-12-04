---
UID: NF:tapi3if.ITSubStreamControl.get_SubStreams
title: ITSubStreamControl::get_SubStreams
author: windows-sdk-content
description: The get_SubStreams method creates a collection of substreams currently available. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateSubStreams method.
old-location: tapi3\itsubstreamcontrol_get_substreams.htm
tech.root: tapi
ms.assetid: 1ea7dca0-9a0b-4966-83ba-0d1f6c5e5ccb
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITSubStreamControl interface [TAPI 2.2],get_SubStreams method, ITSubStreamControl.get_SubStreams, ITSubStreamControl::get_SubStreams, _tapi3_itsubstreamcontrol_get_substreams, get_SubStreams, get_SubStreams method [TAPI 2.2], get_SubStreams method [TAPI 2.2],ITSubStreamControl interface, tapi3.itsubstreamcontrol_get_substreams, tapi3if/ITSubStreamControl::get_SubStreams
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStreamControl.get_SubStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStreamControl::get_SubStreams


## -description


The 
<b>get_SubStreams</b> method creates a collection of substreams currently available. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/848d31e8-f878-4d33-b2b9-2d28e96bd14a">EnumerateSubStreams</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface pointers.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The call appears to have been shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface returned by <b>ITSubStreamControl::get_SubStreams</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>ITSubStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubstream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

