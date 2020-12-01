---
UID: NS:mbnapi.MBN_CONTEXT
title: MBN_CONTEXT (mbnapi.h)
description: The MBN_CONTEXT structure stores information about the connection context.
helpviewer_keywords: ["MBN_CONTEXT","MBN_CONTEXT structure [Microsoft Broadband Networks]","mbn.mbn_context","mbnapi/MBN_CONTEXT"]
old-location: mbn\mbn_context.htm
tech.root: mbn
ms.assetid: 949b1bb3-8cad-45b4-81b7-1f70a76b6c8c
ms.date: 12/05/2018
ms.keywords: MBN_CONTEXT, MBN_CONTEXT structure [Microsoft Broadband Networks], mbn.mbn_context, mbnapi/MBN_CONTEXT
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
targetos: Windows
req.typenames: MBN_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_CONTEXT
 - mbnapi/MBN_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_CONTEXT
---

# MBN_CONTEXT structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_CONTEXT</b> structure stores information about the connection context.

## -struct-fields

### -field contextID

Contains the unique identifier for this context.  This represents the context index in the device or SIM memory.  If it is set to <b>MBN_CONTEXT_ID_APPEND</b>, then the device will find the appropriate index to store the context.

### -field contextType

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_context_type">MBN_CONTEXT_TYPE</a> value that specifies the context type.  An application can use this member to modify the context stored at a particular index using the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectioncontext-setprovisionedcontext">SetProvisionedContext</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectioncontext">IMbnConnectionContext</a>.

### -field accessString

Contains connection-specific access information.  In GSM networks, this would be an access point name (APN) such as "data.thephone-company.com".  In CDMA networks, this might be a special dial code such as "#777" or a NAI (Network Access Identifier) such as "somebody@thephone-company.com".  

This string must not exceed <b>MBN_ACCESSSTRING_LEN</b> characters. For the definition of <b>MBN_ACCESSTRING_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_context_constants">MBN_CONTEXT_CONSTANTS</a>. This string can be empty.  The calling application must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field userName

Contains the user name that is used for authentication.

The string must not exceed <b>MBN_USERNAME_LEN</b> characters.  The calling application must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>. For the definition of <b>MBN_USERNAME_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_context_constants">MBN_CONTEXT_CONSTANTS</a>. The calling application must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field password

Contains the password that is used for authentication.

The string must not exceed <b>MBN_PASSWORD_LEN</b> characters. This string can be empty.  For the definition of <b>MBN_PASSWORD_LEN</b>, see <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_context_constants">MBN_CONTEXT_CONSTANTS</a>. The calling application must free this string by calling <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

### -field compression

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_compression">MBN_COMPRESSION</a> value that specifies whether compression is used in the data link for header and data.

This member is applicable only for GSM devices.

### -field authType

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_auth_protocol">MBN_AUTH_PROTOCOL</a> value that indicates the type of compression used for PDP (Packet Data Protocol) activation.

This member is applicable only for GSM devices.  For CDMA devices, it is set to <b>MBN_AUTH_PROTOCOL_NONE</b>.