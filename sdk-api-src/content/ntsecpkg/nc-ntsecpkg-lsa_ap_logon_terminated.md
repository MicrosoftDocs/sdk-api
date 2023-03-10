---
UID: NC:ntsecpkg.LSA_AP_LOGON_TERMINATED
title: LSA_AP_LOGON_TERMINATED (ntsecpkg.h)
description: Used to notify an authentication package when a logon session terminates. A logon session terminates when the last token referencing the logon session is deleted.
helpviewer_keywords: ["LSA_AP_LOGON_TERMINATED","LSA_AP_LOGON_TERMINATED callback","LsaApLogonTerminated","LsaApLogonTerminated callback function [Security]","_lsa_lsaaplogonterminated","ntsecpkg/LsaApLogonTerminated","security.lsaaplogonterminated"]
old-location: security\lsaaplogonterminated.htm
tech.root: security
ms.assetid: 17e8426a-5a25-48ca-8cef-91bbeda8490c
ms.date: 12/05/2018
ms.keywords: LSA_AP_LOGON_TERMINATED, LSA_AP_LOGON_TERMINATED callback, LsaApLogonTerminated, LsaApLogonTerminated callback function [Security], _lsa_lsaaplogonterminated, ntsecpkg/LsaApLogonTerminated, security.lsaaplogonterminated
req.header: ntsecpkg.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LSA_AP_LOGON_TERMINATED
 - ntsecpkg/LSA_AP_LOGON_TERMINATED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - LsaApLogonTerminated
---

# LSA_AP_LOGON_TERMINATED callback function


## -description

Used to notify an authentication package when a logon session terminates.
			A logon session terminates when the last token referencing the logon session is deleted.

## -parameters

### -param LogonId [in]

Pointer to the logon ID of the session that just ended.

## -remarks

When <b>LsaApLogonTerminated</b> is called, an authentication package should release any resources held for the logon ID, such as credentials created within the LSA. The LSA does not automatically perform this cleanup.

