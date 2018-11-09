---
UID: NS:transportsettingcommon.TRANSPORT_SETTING_ID
title: TRANSPORT_SETTING_ID
author: windows-sdk-content
description: Specifies the transport setting ID used by the SIO_APPLY_TRANSPORT_SETTING and SIO_QUERY_TRANSPORT_SETTING IOCTLs to apply or query the transport setting for a socket.
old-location: winsock\transport_setting_id.htm
tech.root: winsock
ms.assetid: 8ECBF92A-0AF9-4419-A4E8-0EDEF63FCE16
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PTRANSPORT_SETTING_ID, PTRANSPORT_SETTING_ID, PTRANSPORT_SETTING_ID structure pointer [Winsock], TRANSPORT_SETTING_ID, TRANSPORT_SETTING_ID structure [Winsock], transportsettingcommon/PTRANSPORT_SETTING_ID, transportsettingcommon/TRANSPORT_SETTING_ID, winsock.transport_setting_id"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: transportsettingcommon.h
req.include-header: Mstcpip.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - HeaderDef
api_location:
 - transportsettingcommon.h
api_name:
 - TRANSPORT_SETTING_ID
product: Windows
targetos: Windows
req.typenames: TRANSPORT_SETTING_ID, *PTRANSPORT_SETTING_ID
req.redist: 
---

# TRANSPORT_SETTING_ID structure


## -description


The <b>TRANSPORT_SETTING_ID</b> structure specifies the transport setting ID used by the  <a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a> and <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> IOCTLs to apply or query the transport setting for a socket.


## -struct-fields




### -field Guid

The transport setting ID. 


## -remarks



The only transport setting defined for Windows 8 and Windows Server 2012 is for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> capability on a TCP socket. For Windows 10 and Windows Server 2016, there is another transport setting defined as <b>ASSOCIATE_NAMERES_CONTEXT</b>.

The <b>TRANSPORT_SETTING_ID</b> structure is passed as input to the <a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a> and <a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a> 
        IOCTLs. The <b>Guid</b> member determines what transport setting is applied or queried. 

The only transport setting currently defines is for the <b>REAL_TIME_NOTIFICATION_CAPABILITY</b> capability on a TCP socket.




## -see-also




<a href="https://msdn.microsoft.com/35cdf588-0f26-4c88-a898-e1d2ba8203ac">ControlChannelTrigger</a>



<a href="https://msdn.microsoft.com/A008310D-D812-4DCD-A3F2-64FEEEB31DB8">REAL_TIME_NOTIFICATION_SETTING_OUTPUT</a>



<a href="https://msdn.microsoft.com/FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715">SIO_APPLY_TRANSPORT_SETTING</a>



<a href="https://msdn.microsoft.com/3845BE07-A414-4118-96E8-8BEF1DEDB1D3">SIO_QUERY_TRANSPORT_SETTING</a>
 

 

