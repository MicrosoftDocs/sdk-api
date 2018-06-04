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

# IMFShutdown::GetShutdownStatus


## -description



          Queries the status of an earlier call to the <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a> method.
        


## -parameters




### -param pStatus [out]


            Receives a member of the <a href="https://msdn.microsoft.com/a2257260-3f2c-4c6b-88cc-b8927b899782">MFSHUTDOWN_STATUS</a> enumeration.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">

                The <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has not been called on this object.
              

</td>
</tr>
</table>
 




## -remarks



Until <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> is called, the <b>GetShutdownStatus</b> method returns <b>MF_E_INVALIDREQUEST</b>.

If an object's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method is asynchronous, <i>pStatus</i> might receive the value <b>MFSHUTDOWN_INITIATED</b>. When the object is completely shut down, <i>pStatus</i> receives the value <b>MFSHUTDOWN_COMPLETED</b>.




## -see-also




<a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a>
 

 

