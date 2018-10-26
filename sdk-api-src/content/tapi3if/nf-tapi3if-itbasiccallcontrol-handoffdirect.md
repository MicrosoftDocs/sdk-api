---
UID: NF:tapi3if.ITBasicCallControl.HandoffDirect
title: ITBasicCallControl::HandoffDirect
author: windows-sdk-content
description: The HandoffDirect method hands off the call to another application. This indicates that the application no longer requires ownership of the call.
old-location: tapi3\itbasiccallcontrol_handoffdirect.htm
tech.root: TAPI
ms.assetid: a96a3790-ee5d-4983-b69a-30c7af96afd9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: HandoffDirect, HandoffDirect method [TAPI 2.2], HandoffDirect method [TAPI 2.2],ITBasicCallControl interface, ITBasicCallControl interface [TAPI 2.2],HandoffDirect method, ITBasicCallControl.HandoffDirect, ITBasicCallControl::HandoffDirect, _tapi3_itbasiccallcontrol_handoffdirect, tapi3.itbasiccallcontrol_handoffdirect, tapi3if/ITBasicCallControl::HandoffDirect
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITBasicCallControl.HandoffDirect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITBasicCallControl::HandoffDirect


## -description


The 
<b>HandoffDirect</b> method hands off the call to another application. This indicates that the application no longer requires ownership of the call.


## -parameters




### -param pApplicationName [in]

Pointer to <b>BSTR</b> containing the specific application name to hand off call to. Can be full path name or executable name.


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
The <i>pApplicationName</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



Some service providers do not support this operation while streaming is active. The application may need to call 
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">ITStream::StopStream</a> or 
<a href="https://msdn.microsoft.com/fa5028f6-80eb-4076-a81c-c83b462fc27c">ITSubStream::StopSubStream</a> prior to the operation and 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> or 
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">ITSubStream::StartSubStream</a> following completion of the operation.

If the receiving application has not opened the line for the media types involved in the call, the handoff will fail. If TAPI fails to hand off the call, TAPI will call 
<a href="https://msdn.microsoft.com/b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95">Disconnect</a>.

The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pApplicationName</i> parameter and use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95">Disconnect</a>



<a href="https://msdn.microsoft.com/d6d188c9-9cbd-45af-93f0-b78850374919">Handoffs overview</a>



<a href="https://msdn.microsoft.com/a0b4c496-5ee8-4810-8170-8ea505c99f18">ITBasicCallControl</a>



<a href="https://msdn.microsoft.com/931c2fa4-dad6-432d-8f07-bb04b646916b">lineHandoff</a>
 

 

