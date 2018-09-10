---
UID: NS:subauth._SR_SECURITY_DESCRIPTOR
title: "_SR_SECURITY_DESCRIPTOR"
author: windows-sdk-content
description: The SR_SECURITY_DESCRIPTOR structure contains information about the security privileges of the user.
old-location: security\sr_security_descriptor.htm
tech.root: SecAuthN
ms.assetid: 000ffbbe-5750-449b-8237-27c8d3c45454
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSR_SECURITY_DESCRIPTOR, PSR_SECURITY_DESCRIPTOR, PSR_SECURITY_DESCRIPTOR structure pointer [Security], SR_SECURITY_DESCRIPTOR, SR_SECURITY_DESCRIPTOR structure [Security], _SR_SECURITY_DESCRIPTOR, _lsa_sr_security_descriptor, security.sr_security_descriptor, subauth/PSR_SECURITY_DESCRIPTOR, subauth/SR_SECURITY_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: subauth.h
req.include-header: 
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
 - Subauth.h
api_name:
 - SR_SECURITY_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: SR_SECURITY_DESCRIPTOR, *PSR_SECURITY_DESCRIPTOR
req.redist: 
---

# _SR_SECURITY_DESCRIPTOR structure


## -description


The <b>SR_SECURITY_DESCRIPTOR</b> structure contains information about the security <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privileges</a> of the user.


## -struct-fields




### -field Length

Indicates the size in bytes of the structure.


### -field SecurityDescriptor

Indicates the user's security privileges.

