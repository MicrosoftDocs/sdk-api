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

# MBN_CONTEXT structure


## -description


The <b>MBN_CONTEXT</b> structure stores information about the connection context.


## -struct-fields




### -field contextID

Contains the unique identifier for this context.  This represents the context index in the device or SIM memory.  If it is set to <b>MBN_CONTEXT_ID_APPEND</b>, then the device will find the appropriate index to store the context.


### -field contextType

An <a href="https://msdn.microsoft.com/40ab2190-9fc2-43e2-9a8a-29fcaa5b035f">MBN_CONTEXT_TYPE</a> value that specifies the context type.  An application can use this member to modify the context stored at a particular index using the <a href="https://msdn.microsoft.com/738a3037-01a9-465a-a67d-979a29968b68">SetProvisionedContext</a> method of <a href="https://msdn.microsoft.com/a9bc52dc-47f9-4b20-b98d-0287464a89e5">IMbnConnectionContext</a>.


### -field accessString

Contains connection-specific access information.  In GSM networks, this would be an access point name (APN) such as "data.thephone-company.com".  In CDMA networks, this might be a special dial code such as "#777" or a NAI (Network Access Identifier) such as "somebody@thephone-company.com".  

This string must not exceed <b>MBN_ACCESSSTRING_LEN</b> characters. For the definition of <b>MBN_ACCESSTRING_LEN</b>, see <a href="https://msdn.microsoft.com/064ff090-eb45-4cfa-99bd-d92db8397fc3">MBN_CONTEXT_CONSTANTS</a>. This string can be empty.  The calling application must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


### -field userName

Contains the user name that is used for authentication.

The string must not exceed <b>MBN_USERNAME_LEN</b> characters.  The calling application must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>. For the definition of <b>MBN_USERNAME_LEN</b>, see <a href="https://msdn.microsoft.com/064ff090-eb45-4cfa-99bd-d92db8397fc3">MBN_CONTEXT_CONSTANTS</a>. The calling application must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


### -field password

Contains the password that is used for authentication.

The string must not exceed <b>MBN_PASSWORD_LEN</b> characters. This string can be empty.  For the definition of <b>MBN_PASSWORD_LEN</b>, see <a href="https://msdn.microsoft.com/064ff090-eb45-4cfa-99bd-d92db8397fc3">MBN_CONTEXT_CONSTANTS</a>. The calling application must free this string by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>.


### -field compression

An <a href="https://msdn.microsoft.com/fd5cbfba-2eea-4d81-9733-33feb402fd8d">MBN_COMPRESSION</a> value that specifies whether compression is used in the data link for header and data.

This member is applicable only for GSM devices.


### -field authType

An <a href="https://msdn.microsoft.com/7a1858d4-3415-490d-b264-3033cd8f5af7">MBN_AUTH_PROTOCOL</a> value that indicates the type of compression used for PDP (Packet Data Protocol) activation.

This member is applicable only for GSM devices.  For CDMA devices, it is set to <b>MBN_AUTH_PROTOCOL_NONE</b>.

