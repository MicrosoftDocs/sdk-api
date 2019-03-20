---
UID: NS:lmaccess._NET_VALIDATE_PASSWORD_HASH
title: NET_VALIDATE_PASSWORD_HASH (lmaccess.h)
author: windows-sdk-content
description: The NET_VALIDATE_PASSWORD_HASH structure contains a password hash.
old-location: netmgmt\net_validate_password_hash.htm
tech.root: NetMgmt
ms.assetid: 884e5b8c-1288-454e-862d-323d79123356
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNET_VALIDATE_PASSWORD_HASH, NET_VALIDATE_PASSWORD_HASH, NET_VALIDATE_PASSWORD_HASH structure [Network Management], PNET_VALIDATE_PASSWORD_HASH, PNET_VALIDATE_PASSWORD_HASH structure pointer [Network Management], lmaccess/NET_VALIDATE_PASSWORD_HASH, lmaccess/PNET_VALIDATE_PASSWORD_HASH, netmgmt.net_validate_password_hash"
ms.topic: struct
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Lmaccess.h
api_name:
 - NET_VALIDATE_PASSWORD_HASH
product: Windows
targetos: Windows
req.typenames: NET_VALIDATE_PASSWORD_HASH, *PNET_VALIDATE_PASSWORD_HASH
req.redist: 
---

# NET_VALIDATE_PASSWORD_HASH structure


## -description


The <b>NET_VALIDATE_PASSWORD_HASH</b> structure contains a password hash.


## -struct-fields




### -field Length

Specifies the length of this structure.


### -field Hash

Password hash.


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa370689(v=VS.85).aspx">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa370687(v=VS.85).aspx">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a> structures contain a <b>NET_VALIDATE_PASSWORD_HASH</b> structure. The <a href="https://msdn.microsoft.com/1e6ea28a-a007-4cd1-b5d6-686bcf019fa1">NET_VALIDATE_PERSISTED_FIELDS</a> structure contains a pointer to this structure. 




## -see-also




<a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

