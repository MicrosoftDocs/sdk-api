---
UID: NS:webservices._WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE
title: "_WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE"
author: windows-sdk-content
description: The type for specifying a symmetric cryptographic key as raw bytes.
old-location: wsw\ws_raw_symmetric_security_key_handle.htm
tech.root: wsw
ms.assetid: 8c2c664b-2ee4-4647-a219-119eb5c5a0f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE, WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE structure [Web Services for Windows], _WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE, webservices/WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE, wsw.ws_raw_symmetric_security_key_handle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WebServices.h
api_name:
 - WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE
product: Windows
targetos: Windows
req.typenames: WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE
req.redist: 
---

# _WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE structure


## -description


The type for specifying a symmetric cryptographic key as raw bytes.
            


## -struct-fields




### -field keyHandle

The base type from which this type and all other key handle types derive.
                


### -field rawKeyBytes

The cryptographic key as raw bytes.  It is strongly recommended that
after the key is supplied in this form to any API, it is immediately
cleared using SecureZeroMemory.
                

