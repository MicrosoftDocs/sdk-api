---
UID: NF:sspi.SspiIsPromptingNeeded
title: SspiIsPromptingNeeded function (sspi.h)
description: Indicates whether an error returned after a call to either the InitializeSecurityContext or the AcceptSecurityContext function requires an additional call to the SspiPromptForCredentials function.
helpviewer_keywords: ["SspiIsPromptingNeeded","SspiIsPromptingNeeded function [Security]","security.sspiispromptingneeded","sspi/SspiIsPromptingNeeded"]
old-location: security\sspiispromptingneeded.htm
tech.root: security
ms.assetid: aaafcf49-df28-45e9-8c06-e57863a2e300
ms.date: 12/05/2018
ms.keywords: SspiIsPromptingNeeded, SspiIsPromptingNeeded function [Security], security.sspiispromptingneeded, sspi/SspiIsPromptingNeeded
req.header: sspi.h
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
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SspiIsPromptingNeeded
 - sspi/SspiIsPromptingNeeded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-0.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - SspiIsPromptingNeeded
---

# SspiIsPromptingNeeded function


## -description

Indicates whether an error returned after a call to either the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext</a> or the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext</a> function requires an additional call to the <a href="/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa">SspiPromptForCredentials</a> function.

## -parameters

### -param ErrorOrNtStatus [in]

The error to test.

## -returns

<b>TRUE</b> if the error specified by the <i>ErrorOrNtStatus</i> parameter indicates that an additional call to <a href="/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa">SspiPromptForCredentials</a> is necessary; otherwise, <b>FALSE</b>.