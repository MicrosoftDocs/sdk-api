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

# _TCP_ESTATS_BANDWIDTH_RW_v0 structure


## -description


The <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> structure contains read/write configuration information for extended TCP statistics on bandwidth estimation for a TCP connection.


## -struct-fields




### -field EnableCollectionOutbound

A value that indicates if extended statistics on a TCP connection should be collected for outbound bandwidth estimation. 

If this member is set to <b>TcpBoolOptEnabled</b>, extended statistics on the TCP connection for outbound bandwidth estimation are enabled. If this member is set to <b>TcpBoolOptDisabled</b>, extended statistics on the TCP connection for outbound bandwidth estimation are disabled. If this member is set to <b>TcpBoolOptUnchanged</b>, extended statistics on the TCP connection for outbound bandwidth estimation are left unchanged. 

The default state for this member when not set is disabled.


### -field EnableCollectionInbound

A value that indicates if extended statistics on a TCP connection should be collected for inbound bandwidth estimation. 

If this member is set to <b>TcpBoolOptEnabled</b>, extended statistics on the TCP connection for inbound bandwidth estimation are enabled. If this member is set to <b>TcpBoolOptDisabled</b>, extended statistics on the TCP connection for inbound bandwidth estimation are disabled. If this member is set to <b>TcpBoolOptUnchanged</b>, extended statistics on the TCP connection for inbound bandwidth estimation are unchanged. 

The default state for this member when not set is disabled.


## -remarks



The <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> structure is used as part of the TCP extended statistics feature available on Windows Vista and later. 

The <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> is defined as version 0 of the structure for  read/write configuration information on bandwidth estimation for a TCP connection.  

Extended TCP statistics on bandwidth estimation for a TCP connection are enabled and disabled using this structure and the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsBandwidth</b> is passed in the <i>EstatsType</i> parameter.

The <i>Offset</i> parameter passed to the <a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a> and <a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a> functions is currently unused and must be set to 0. Consequently, the <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> structure pointed to by the <i>Rw</i> parameter when the <i>EstatsType</i> parameter is set to <b>TcpConnectionEstatsBandwidth</b> must have both the <b>EnableCollectionOutbound</b> and <b>EnableCollectionInbound</b> structure members set to the preferred values in a single call to the  <b>SetPerTcp6ConnectionEStats</b> and <b>SetPerTcpConnectionEStats</b> functions.

The <b>TCP_ESTATS_BANDWIDTH_RW_v0</b> structure is retrieved by calls to  the <a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a> or <a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a> functions when <b>TcpConnectionEstatsBandwidth</b> is passed in the <i>EstatsType</i> parameter. 




## -see-also




<a href="https://msdn.microsoft.com/291aabe7-a4e7-4cc7-9cf3-4a4bc021e15e">GetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/71b9d795-6050-4a1a-9949-2c970801f52c">GetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/89ace750-ec32-46cb-8526-233f847ba9f4">SetPerTcp6ConnectionEStats</a>



<a href="https://msdn.microsoft.com/96d838ca-69e3-4a73-b969-3e6e810a0a69">SetPerTcpConnectionEStats</a>



<a href="https://msdn.microsoft.com/68f8f797-06fb-4286-88bc-220c54977575">TCP_BOOLEAN_OPTIONAL</a>



<a href="https://msdn.microsoft.com/96f55528-e74a-4360-a7a2-54ba19c3a284">TCP_ESTATS_TYPE</a>
 

 

