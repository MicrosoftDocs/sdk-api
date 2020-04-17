---
UID: NF:ntsecapi.AuditFree
title: AuditFree function (ntsecapi.h)
description: Frees the memory allocated by audit functions for the specified buffer.helpviewer_keywords: ["AuditFree","AuditFree function [Security]","ntsecapi/AuditFree","security.auditfree_func"]
old-location: security\auditfree_func.htm
tech.root: SecAuthZ
ms.assetid: 697baf9b-91c4-4a88-a190-e9f6812e08af
ms.date: 12/05/2018
ms.keywords: AuditFree, AuditFree function [Security], ntsecapi/AuditFree, security.auditfree_func
f1_keywords:
- ntsecapi/AuditFree
dev_langs:
- c++
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-Security-audit-l1-1-0.dll
- sechost.dll
- API-MS-Win-Security-audit-l1-1-1.dll
api_name:
- AuditFree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuditFree function


## -description


The <b>AuditFree</b> function frees the memory allocated by audit functions for the specified buffer. 


## -parameters




### -param Buffer [in]

A pointer to the buffer to free.


