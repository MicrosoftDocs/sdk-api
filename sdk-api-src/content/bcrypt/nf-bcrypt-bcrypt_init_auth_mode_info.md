---
UID: NF:bcrypt.BCRYPT_INIT_AUTH_MODE_INFO
title: BCRYPT_INIT_AUTH_MODE_INFO macro
author: windows-sdk-content
description: Initializes a BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure for use in calls to BCryptEncrypt and BCryptDecrypt functions.
old-location: security\bcrypt_init_auth_mode_info.htm
tech.root: seccng
ms.assetid: 5c825337-bd60-48e4-9d71-bfd1d38ab171
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BCRYPT_INIT_AUTH_MODE_INFO, BCRYPT_INIT_AUTH_MODE_INFO macro [Security], bcrypt/BCRYPT_INIT_AUTH_MODE_INFO, security.bcrypt_init_auth_mode_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
 - Bcrypt.h
api_name:
 - BCRYPT_INIT_AUTH_MODE_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCRYPT_INIT_AUTH_MODE_INFO macro


## -description


The <b>BCRYPT_INIT_AUTH_MODE_INFO</b> macro  initializes a <a href="https://msdn.microsoft.com/en-us/library/Cc562981(v=VS.85).aspx">BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</a> structure for use in calls to <a href="https://msdn.microsoft.com/en-us/library/Aa375421(v=VS.85).aspx">BCryptEncrypt</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa375391(v=VS.85).aspx">BCryptDecrypt</a> functions.


## -parameters




### -param _AUTH_INFO_STRUCT_

The BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure to initialize.

