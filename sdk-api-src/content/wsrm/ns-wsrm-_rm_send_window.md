---
UID: NS:wsrm._RM_SEND_WINDOW
title: "_RM_SEND_WINDOW"
author: windows-sdk-content
description: The RM_SEND_WINDOW structure specifies the Reliable Multicast send window. This structure is used with the RM_RATE_WINDOW_SIZE socket option.
old-location: winsock\rm_send_window.htm
old-project: WinSock
ms.assetid: 7ce84d2e-a52f-4652-b24a-55c94b7c120b
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: RM_SEND_WINDOW, RM_SEND_WINDOW structure [Winsock], _RM_SEND_WINDOW, winsock.rm_send_window, wsrm/RM_SEND_WINDOW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RM_SEND_WINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsrm.h
api_name:
-	RM_SEND_WINDOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _RM_SEND_WINDOW structure


## -description


The <b>RM_SEND_WINDOW</b> structure specifies the Reliable Multicast send window. This structure is used with the <a href="https://msdn.microsoft.com/cb99960e-428b-4ef1-a6a5-e4bdb497c771">RM_RATE_WINDOW_SIZE</a> socket option.


## -struct-fields




### -field RateKbitsPerSec

Transmission rate for the send window, in kilobits per second.


### -field WindowSizeInMSecs

Window size for the send window, in milliseconds.


### -field WindowSizeInBytes

Window size for the session, in bytes.


## -remarks



Any combination of the three available members may be set for a given socket option call. For example, one, any two, or all three members may be specified during a <a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a> function call. Regardless of settings, Windows enforces the following ratio: <b>TransmissionRate</b> == (<b>WindowSizeBytes</b>/<b>WindowSizeMSecs</b>) * 8. As such, setting any two parameters effectively sets the third to ensure optimum performance. 

The combination of these members can affect the resources used on a PGM sender's computer. For example, a large transmission rate value combined with a large window size results in more required buffer space.




## -see-also




<a href="https://msdn.microsoft.com/cb99960e-428b-4ef1-a6a5-e4bdb497c771">IPPROTO_RM Socket Options</a>



<a href="https://msdn.microsoft.com/81c203ed-739f-4a06-99a1-9a99c6164edc">Reliable Multicast Programming</a>



<a href="https://msdn.microsoft.com/e2831f76-4499-45b6-bc60-2908ec3a246c">Socket Options</a>



<a href="https://msdn.microsoft.com/3a6960c9-0c04-4403-aee1-ce250459dc30">setsockopt</a>
 

 

