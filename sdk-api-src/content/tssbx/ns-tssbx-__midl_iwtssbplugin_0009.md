---
UID: NS:tssbx.__MIDL_IWTSSBPlugin_0009
title: "__MIDL_IWTSSBPlugin_0009"
author: windows-driver-content
description: Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\wtssbx_session_info.htm
old-project: TermServ
ms.assetid: d0c142a9-2495-46e6-b53b-0c415bddb0b2
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: WTSSBX_SESSION_INFO, WTSSBX_SESSION_INFO structure [Remote Desktop Services], __MIDL_IWTSSBPlugin_0009, termserv.wtssbx_session_info, tssbx/WTSSBX_SESSION_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tssbx.h
api_name:
-	WTSSBX_SESSION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL_IWTSSBPlugin_0009 structure


## -description


Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).


## -struct-fields




### -field wszUserName

The user name that is associated with the session. The name cannot exceed 104 characters.


### -field wszDomainName

The domain name of the user. The name cannot exceed 256 characters.


### -field ApplicationType

The name of the program that should be run after the session is created. The name cannot exceed 256 characters.


### -field dwSessionId

The session identifier.


### -field CreateTime

The time that the session was initiated.


### -field DisconnectTime

The time that the user disconnected from the session.


### -field SessionState

A value of the <a href="https://msdn.microsoft.com/d31118c5-56a3-4792-83fd-fdd3cd7a79ea">WTSSBX_SESSION_STATE</a> enumeration type that indicates the state of the session.


## -see-also




<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

