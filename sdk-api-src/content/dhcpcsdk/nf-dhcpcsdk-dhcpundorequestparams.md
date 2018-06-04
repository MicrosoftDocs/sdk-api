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

# DhcpUndoRequestParams function


## -description


The 
<b>DhcpUndoRequestParams</b> function removes persistent requests previously made with a 
<b>DhcpRequestParams</b> function call.


## -parameters




### -param Flags [in]

Reserved. Must be zero.


### -param Reserved [in]

Reserved for future use. Must be set to <b>NULL</b>.


### -param AdapterName [in]

Name of the adapter for which information is no longer required.  Must be under 256 characters.

<div class="alert"><b>Note</b>  This parameter is no longer used.</div>
<div> </div>

### -param RequestIdStr [in]

Application identifier (ID) originally used to make a persistent request. This string must match the <i>RequestIdStr</i> parameter used in the 
<b>DhcpRequestParams</b> function call that obtained the corresponding persistent request. Note that this must match the previous application identifier (ID) used, and must be a printable string with no special characters (commas, backslashes, colons, or other illegal characters may not be used).


## -returns



Returns ERROR_SUCCESS upon successful completion. Otherwise, returns a Windows error code.




## -remarks



Persistent requests are typically made by the setup or installer process associated with the application. When appropriate, the setup or installer process would likely make the 
<b>DhcpUndoRequestParams</b> function call to cancel its associated persistent request.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a>



<a href="https://msdn.microsoft.com/5fcbd1d9-8170-4c2b-ac98-6c04107c46e7">DhcpRequestParams</a>
 

 

