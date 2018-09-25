---
UID: NF:tapi3if.ITSubStreamControl.EnumerateSubStreams
title: ITSubStreamControl::EnumerateSubStreams
author: windows-sdk-content
description: The EnumerateSubStreams method enumerates currently available media substreams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_SubStreams method.
old-location: tapi3\itsubstreamcontrol_enumeratesubstreams.htm
tech.root: tapi
ms.assetid: 848d31e8-f878-4d33-b2b9-2d28e96bd14a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: EnumerateSubStreams, EnumerateSubStreams method [TAPI 2.2], EnumerateSubStreams method [TAPI 2.2],ITSubStreamControl interface, ITSubStreamControl interface [TAPI 2.2],EnumerateSubStreams method, ITSubStreamControl.EnumerateSubStreams, ITSubStreamControl::EnumerateSubStreams, _tapi3_itsubstreamcontrol_enumeratesubstreams, tapi3.itsubstreamcontrol_enumeratesubstreams, tapi3if/ITSubStreamControl::EnumerateSubStreams
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
 - ITSubStreamControl.EnumerateSubStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStreamControl::EnumerateSubStreams


## -description


The 
<b>EnumerateSubStreams</b> method enumerates currently available media substreams. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
<a href="https://msdn.microsoft.com/1ea7dca0-9a0b-4966-83ba-0d1f6c5e5ccb">get_SubStreams</a> method.


## -parameters




### -param ppEnumSubStream [out]

Pointer to 
<a href="https://msdn.microsoft.com/d9076a32-983e-48d4-b025-5fc770156df6">IEnumSubStream</a> enumeration of substreams.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumSubStream</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/d9076a32-983e-48d4-b025-5fc770156df6">IEnumSubStream</a> interface returned by <b>ITSubStreamControl::EnumerateSubStreams</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>IEnumSubStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

