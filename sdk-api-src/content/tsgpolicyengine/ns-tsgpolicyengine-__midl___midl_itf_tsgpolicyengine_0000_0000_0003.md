---
UID: NS:tsgpolicyengine.__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003
title: "__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003"
author: windows-sdk-content
description: This structure contains information about a connection event.
old-location: termserv\aaaccountingdata.htm
tech.root: termserv
ms.assetid: 1c79f910-8dd9-47dc-80d1-f6252f0a43dd
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AAAccountingData, AAAccountingData structure [Remote Desktop Services], __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003, termserv.aaaccountingdata, tsgpolicyengine/AAAccountingData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
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
 - TSGPolicyEngine.h
api_name:
 - AAAccountingData
product: Windows
targetos: Windows
req.typenames: AAAccountingData
req.redist: 
---

# __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003 structure


## -description


This structure contains information about a connection event.


## -struct-fields




### -field userName

The user name.


### -field clientName

The name of the client computer.


### -field authType

A value of the <a href="https://msdn.microsoft.com/ff80f8ac-8378-4087-aa95-a081d2dd710a">AAAuthSchemes</a> enumeration type that specifies the type of authentication used to connect to RD Gateway.


### -field resourceName

The name of the remote computer.


### -field portNumber

The port number of the remote computer used by the connection.


### -field protocolName

The name of the protocol used by the connection.


### -field numberOfBytesReceived

The number of bytes sent from the client to the remote computer.


### -field numberOfBytesTransfered

The number of bytes sent from the remote computer to the client.


### -field reasonForDisconnect

The reason the connection was disconnected.


### -field mainSessionId

A unique identifier assigned to the connection  by RD Gateway.


### -field subSessionId

A unique identifier assigned to the subsession by RD Gateway.

