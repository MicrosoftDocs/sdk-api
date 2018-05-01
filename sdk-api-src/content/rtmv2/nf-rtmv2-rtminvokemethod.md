---
UID: NF:rtmv2.RtmInvokeMethod
title: RtmInvokeMethod function
author: windows-driver-content
description: The RtmInvokeMethod function invokes a method exported by another client.
old-location: rras\rtminvokemethod.htm
old-project: RRAS
ms.assetid: 97506565-2fa7-4ff7-b397-7ab712759a5d
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RtmInvokeMethod, RtmInvokeMethod function [RAS], _rtmv2ref_rtminvokemethod, rras.rtminvokemethod, rtmv2/RtmInvokeMethod
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RTM_EVENT_TYPE, *PRTM_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rtm.dll
api_name:
-	RtmInvokeMethod
product: Windows
targetos: Windows
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtmInvokeMethod function


## -description


The 
<b>RtmInvokeMethod</b> function invokes a method exported by another client.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/2b952ea2-cf33-49e3-ae31-a14b0907a1b5">RtmRegisterEntity</a>.


### -param EntityHandle [in]

Handle to the client whose methods are being invoked.


### -param Input [in]

Pointer to an 
<a href="https://msdn.microsoft.com/1f900e85-c522-47c9-bfc8-5a1c1d01ab78">RTM_ENTITY_METHOD_INPUT</a> structure that contains the method to be invoked and a common input buffer.


### -param OutputSize [in, out]

On input, <i>OutputSize</i> is a pointer to a <b>UINT</b> value that specifies the size, in bytes, of <i>Output</i>. 




On output, <i>OutputSize</i> receives a pointer to a <b>UINT</b> value that specifies the actual size, in bytes, of <i>Output</i>.


### -param Output [out]

Receives a pointer to an array of 
<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a> structures. Each structure consists of a (method identifier, correct output) tuple.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



For sample code using this function, see 
<a href="https://msdn.microsoft.com/55b2a03f-498c-4321-891b-747f4baea10d">Obtain and Call the Exported Methods for a Client</a>.




## -see-also




<a href="https://msdn.microsoft.com/1f900e85-c522-47c9-bfc8-5a1c1d01ab78">RTM_ENTITY_METHOD_INPUT</a>



<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a>



<a href="https://msdn.microsoft.com/492bb2bf-5b35-4eef-a039-3d3e1137220f">RtmBlockMethods</a>



<a href="https://msdn.microsoft.com/186f4a55-d46b-42ab-b092-dc036b011594">RtmGetEntityMethods</a>
 

 

