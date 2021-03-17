---
UID: NS:tsgpolicyengine.__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003
title: AAAccountingData (tsgpolicyengine.h)
description: This structure contains information about a connection event.
helpviewer_keywords: ["AAAccountingData","AAAccountingData structure [Remote Desktop Services]","__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003","termserv.aaaccountingdata","tsgpolicyengine/AAAccountingData"]
old-location: termserv\aaaccountingdata.htm
tech.root: TermServ
ms.assetid: 1c79f910-8dd9-47dc-80d1-f6252f0a43dd
ms.date: 12/05/2018
ms.keywords: AAAccountingData, AAAccountingData structure [Remote Desktop Services], __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003, termserv.aaaccountingdata, tsgpolicyengine/AAAccountingData
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
targetos: Windows
req.typenames: AAAccountingData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003
 - tsgpolicyengine/__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003
 - AAAccountingData
 - tsgpolicyengine/AAAccountingData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TSGPolicyEngine.h
api_name:
 - AAAccountingData
---

# AAAccountingData structure


## -description

This structure contains information about a connection event.

## -struct-fields

### -field userName

The user name.

### -field clientName

The name of the client computer.

### -field authType

A value of the <a href="/windows/win32/api/tsgpolicyengine/ne-tsgpolicyengine-aaauthschemes">AAAuthSchemes</a> enumeration type that specifies the type of authentication used to connect to RD Gateway.

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

