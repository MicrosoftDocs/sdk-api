---
UID: NF:mfidl.IMFShutdown.GetShutdownStatus
title: IMFShutdown::GetShutdownStatus
author: windows-sdk-content
description: Queries the status of an earlier call to the IMFShutdown::Shutdown method.
old-location: mf\imfshutdown_getshutdownstatus.htm
tech.root: medfound
ms.assetid: 8cf5f5f3-a3ad-4745-87e8-764ed118477a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 8cf5f5f3-a3ad-4745-87e8-764ed118477a, GetShutdownStatus, GetShutdownStatus method [Media Foundation], GetShutdownStatus method [Media Foundation],IMFShutdown interface, IMFShutdown interface [Media Foundation],GetShutdownStatus method, IMFShutdown.GetShutdownStatus, IMFShutdown::GetShutdownStatus, mf.imfshutdown_getshutdownstatus, mfidl/IMFShutdown::GetShutdownStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFShutdown.GetShutdownStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
The <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> method has not been called on this object.
              

</td>
</tr>
</table>
 




## -remarks



Until <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> is called, the <b>GetShutdownStatus</b> method returns <b>MF_E_INVALIDREQUEST</b>.

If an object's <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">Shutdown</a> method is asynchronous, <i>pStatus</i> might receive the value <b>MFSHUTDOWN_INITIATED</b>. When the object is completely shut down, <i>pStatus</i> receives the value <b>MFSHUTDOWN_COMPLETED</b>.




## -see-also




<a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a>
 

 

