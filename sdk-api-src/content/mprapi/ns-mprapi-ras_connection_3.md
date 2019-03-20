---
UID: NS:mprapi._RAS_CONNECTION_3
title: RAS_CONNECTION_3 (mprapi.h)
author: windows-sdk-content
description: The RAS_CONNECTION_3 structure contains information for the connection, including the Globally Unique Identifier (GUID) that identifies the connection and the quarantine state of the connection.
old-location: rras\ras_connection_3.htm
tech.root: RRAS
ms.assetid: f474563e-01c5-4f2a-aec4-477e0ffc7ab2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PRAS_CONNECTION_3, PRAS_CONNECTION_3, PRAS_CONNECTION_3 structure pointer [RAS], RAS_CONNECTION_3, RAS_CONNECTION_3 structure [RAS], mprapi/PRAS_CONNECTION_3, mprapi/RAS_CONNECTION_3, rras.ras_connection_3"
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Mprapi.h
api_name:
 - RAS_CONNECTION_3
product: Windows
targetos: Windows
req.typenames: RAS_CONNECTION_3, *PRAS_CONNECTION_3
req.redist: 
---

# RAS_CONNECTION_3 structure


## -description


The 
<b>RAS_CONNECTION_3</b> structure contains information for the connection, including the Globally Unique Identifier (GUID) that identifies the connection and the quarantine state of the connection.




## -struct-fields




### -field dwVersion

The version of the <b>RAS_CONNECTION_3</b> structure used.


### -field dwSize

The size, in bytes, of this <b>RAS_CONNECTION_3</b> structure.


### -field hConnection

A handle to the connection.


### -field wszUserName

A null-terminated Unicode string that contains the name of the user logged on to the connection.


### -field dwInterfaceType

A <a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.


### -field guid

A GUID  that identifies the connection. For incoming connections, this GUID is valid only as long as the connection is active.


### -field PppInfo3

A 
<a href="https://msdn.microsoft.com/cc231775-83bc-45d5-8bd8-7ac4cf5f09ff">PPP_INFO_3</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.


### -field rasQuarState

A <a href="https://msdn.microsoft.com/df0193c0-a40b-464f-8c82-08d1fe66fdf9">RAS_QUARANTINE_STATE</a> structure that specifies the Network Access Protection (NAP) quarantine state of the connection.


### -field timer

A FILETIME structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped. This value is valid only if <b>rasQuarState</b> has a value of <b>RAS_QUAR_STATE_PROBATION</b>.


## -see-also




<a href="https://msdn.microsoft.com/58fea0ca-b7c1-4d32-bcfc-10b41e101f30">MprAdminAcceptReauthentication</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/8c31d345-8f57-47f5-a021-e399f7ccca5d">MprAdminConnectionHangupNotification3</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

