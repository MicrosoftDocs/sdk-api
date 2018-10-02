---
UID: NS:schannel._SCH_CRED_SECRET_PRIVKEY
title: "_SCH_CRED_SECRET_PRIVKEY"
author: windows-sdk-content
description: Contains private key information needed to authenticate a client or server.
old-location: security\sch_cred_secret_privkey.htm
tech.root: secauthn
ms.assetid: 3d637716-e4cd-427c-bc80-7d0ace6ac521
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PSCH_CRED_SECRET_PRIVKEY, PSCH_CRED_SECRET_PRIVKEY, PSCH_CRED_SECRET_PRIVKEY structure pointer [Security], SCH_CRED_SECRET_PRIVKEY, SCH_CRED_SECRET_PRIVKEY structure [Security], _SCH_CRED_SECRET_PRIVKEY, _ssp_sch_cred_secret_privkey, schannel/PSCH_CRED_SECRET_PRIVKEY, schannel/SCH_CRED_SECRET_PRIVKEY, security.sch_cred_secret_privkey"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: schannel.h
req.include-header: Schnlsp.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - Schannel.h
api_name:
 - SCH_CRED_SECRET_PRIVKEY
product: Windows
targetos: Windows
req.typenames: SCH_CRED_SECRET_PRIVKEY, *PSCH_CRED_SECRET_PRIVKEY
req.redist: 
---

# _SCH_CRED_SECRET_PRIVKEY structure


## -description


<p class="CCE_Message">[The <b>SCH_CRED_SECRET_PRIVKEY</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/8398e029-473e-488f-a861-c7ceae07e678">SCHANNEL_CRED</a> structure.]

The <b>SCH_CRED_SECRET_PRIVKEY</b> structure contains <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> information needed to authenticate a client or server.


## -struct-fields




### -field dwType

Must always be set to SCHANNEL_SECRET_PRIVKEY.


### -field pPrivateKey

Pointer to an encrypted private key.


### -field cbPrivateKey

Number of bytes in the encrypted private key.


### -field pszPassword

Pointer to a null-terminated string that Schannel uses to decrypt the private key.

