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

# _RADIUS_CODE enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_CODE</b> enumeration type enumerates the possible RADIUS packet codes.


## -enum-fields




### -field rcUnknown

The packet type is unrecognized. This is used to indicate that the disposition of a request is not being set by this extension DLL.


### -field rcAccessRequest

RADIUS Access-Request packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field rcAccessAccept

RADIUS Access-Accept packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field rcAccessReject

RADIUS Access-Reject packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field rcAccountingRequest

RADIUS Accounting-Request packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field rcAccountingResponse

RADIUS Accounting-Response packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84056">RFC 2866</a> for more information.


### -field rcAccessChallenge

RADIUS Access-Challenge packet. See 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84055">RFC 2865</a> for more information.


### -field rcDiscard

The packet was discarded.


## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="https://msdn.microsoft.com/96e88037-1131-4f7a-9c34-0e86762361db">SetResponseType</a>
 

 

