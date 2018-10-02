---
UID: NS:mbnapi.MBN_CONTEXT
title: MBN_CONTEXT
author: windows-sdk-content
description: The MBN_CONTEXT structure stores information about the connection context.
old-location: mbn\mbn_context.htm
tech.root: mbn
ms.assetid: 949b1bb3-8cad-45b4-81b7-1f70a76b6c8c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MBN_CONTEXT, MBN_CONTEXT structure [Microsoft Broadband Networks], mbn.mbn_context, mbnapi/MBN_CONTEXT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - MBN_CONTEXT
product: Windows
targetos: Windows
req.typenames: MBN_CONTEXT
req.redist: 
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

