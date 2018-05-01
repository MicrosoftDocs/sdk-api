---
UID: NS:mprapi._RAS_CONNECTION_2
title: "_RAS_CONNECTION_2"
author: windows-driver-content
description: The RAS_CONNECTION_2 structure contains information for a connection, including the Globally Unique Identifier (GUID) that identifies the connection.
old-location: rras\ras_connection_2.htm
old-project: RRAS
ms.assetid: 5dcc20f0-7447-4256-9dde-18a4a3c95816
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PRAS_CONNECTION_2, PRAS_CONNECTION_2, PRAS_CONNECTION_2 structure pointer [RAS], RAS_CONNECTION_2, RAS_CONNECTION_2 structure [RAS], _RAS_CONNECTION_2, _mpr_ras_connection_2, mprapi/PRAS_CONNECTION_2, mprapi/RAS_CONNECTION_2, rras.ras_connection_2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: RAS_CONNECTION_2, *PRAS_CONNECTION_2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mprapi.h
api_name:
-	RAS_CONNECTION_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _RAS_CONNECTION_2 structure


## -description


The 
<b>RAS_CONNECTION_2</b> structure contains information for a connection, including the Globally Unique Identifier (GUID) that identifies the connection.


## -struct-fields




### -field hConnection

A handle to the connection.


### -field wszUserName

A null-terminated Unicode string that contains the name of the user logged on to the connection.


### -field dwInterfaceType

A <a href="https://msdn.microsoft.com/9b957ab0-0c5d-4478-914a-4837e6bbd56a">ROUTER_INTERFACE_TYPE</a> enumeration that identifies the type of connection interface.


### -field guid

A GUID  that identifies the connection. For incoming connections, this GUID is valid only as long as the connection is active.


### -field PppInfo2

A 
<a href="https://msdn.microsoft.com/5fe87e87-6199-4a96-8e76-1838e515116e">PPP_INFO_2</a> structure that contains Point-to-Point (PPP) projection operation information for a connection.


## -see-also




<a href="https://msdn.microsoft.com/58fea0ca-b7c1-4d32-bcfc-10b41e101f30">MprAdminAcceptReauthentication</a>



<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/8c31d345-8f57-47f5-a021-e399f7ccca5d">MprAdminConnectionHangupNotification3</a>



<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS Administration Structures</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

