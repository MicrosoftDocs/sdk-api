---
UID: NF:sspi.SspiIsPromptingNeeded
title: SspiIsPromptingNeeded function
author: windows-sdk-content
description: Indicates whether an error returned after a call to either the InitializeSecurityContext or the AcceptSecurityContext function requires an additional call to the SspiPromptForCredentials function.
old-location: security\sspiispromptingneeded.htm
tech.root: SecAuthN
ms.assetid: aaafcf49-df28-45e9-8c06-e57863a2e300
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SspiIsPromptingNeeded, SspiIsPromptingNeeded function [Security], security.sspiispromptingneeded, sspi/SspiIsPromptingNeeded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SspiIsPromptingNeeded
: 
---

# SspiIsPromptingNeeded function


## -description


Indicates whether an error returned after a call to either the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> or the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext</a> function requires an additional call to the <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> function.


## -parameters




### -param ErrorOrNtStatus [in]

The error to test.


## -returns



<b>TRUE</b> if the error specified by the <i>ErrorOrNtStatus</i> parameter indicates that an additional call to <a href="https://msdn.microsoft.com/2af2ac00-0e91-4384-9ffa-3e100df218c1">SspiPromptForCredentials</a> is necessary; otherwise, <b>FALSE</b>.



