---
UID: NF:mfidl.IMFProtectedEnvironmentAccess.Call
title: IMFProtectedEnvironmentAccess::Call
author: windows-sdk-content
description: Allows content protection systems to access the protected environment.
old-location: mf\imfprotectedenvironmentaccess_call.htm
tech.root: medfound
ms.assetid: 805473c4-a2c9-483a-9a2c-29a9c63dd58c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Call, Call method [Media Foundation], Call method [Media Foundation],IMFProtectedEnvironmentAccess interface, IMFProtectedEnvironmentAccess interface [Media Foundation],Call method, IMFProtectedEnvironmentAccess.Call, IMFProtectedEnvironmentAccess::Call, mf.imfprotectedenvironmentaccess_call, mfidl/IMFProtectedEnvironmentAccess::Call
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - Mfidl.h
api_name:
 - IMFProtectedEnvironmentAccess.Call
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFProtectedEnvironmentAccess::Call


## -description


Allows content protection systems to access the protected environment.


## -parameters




### -param inputLength

The length in bytes of the input data.


### -param input

A pointer to the input data.


### -param outputLength

The length in bytes of the output data.


### -param output

A pointer to the output data.


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
</table>
 




## -remarks



See  <a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a> for an example of how to create an <a href="https://msdn.microsoft.com/2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4">IMFProtectedEnvironmentAccess</a> object and use the <b>Call</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2cd93bc9-4a42-4e16-80aa-4ecf5900f5e4">IMFProtectedEnvironmentAccess</a>



<a href="https://msdn.microsoft.com/B16BEFFD-26CF-4598-96A4-098C3E3AA51C">MFCreateProtectedEnvironmentAccess</a>
 

 

