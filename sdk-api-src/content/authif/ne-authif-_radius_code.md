---
UID: NE:authif._RADIUS_CODE
title: "_RADIUS_CODE"
author: windows-driver-content
description: The RADIUS_CODE enumeration type enumerates the possible RADIUS packet codes.
old-location: nps\IAS_radius_code.htm
old-project: Nps
ms.assetid: cb971643-82ca-4302-a961-9d567da04c27
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: RADIUS_CODE, RADIUS_CODE enumeration [Network Policy Server], _RADIUS_CODE, _ias_radius_code, authif/RADIUS_CODE, authif/rcAccessAccept, authif/rcAccessChallenge, authif/rcAccessReject, authif/rcAccessRequest, authif/rcAccountingRequest, authif/rcAccountingResponse, authif/rcDiscard, authif/rcUnknown, ias.radius_code, nps.IAS_radius_code, rcAccessAccept, rcAccessChallenge, rcAccessReject, rcAccessRequest, rcAccountingRequest, rcAccountingResponse, rcDiscard, rcUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RADIUS_CODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	AuthIf.h
api_name:
-	RADIUS_CODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

