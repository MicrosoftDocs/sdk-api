---
UID: NF:cryptuiapi.CryptUIWizFreeDigitalSignContext
title: CryptUIWizFreeDigitalSignContext function
author: windows-sdk-content
description: Frees the CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure allocated by the CryptUIWizDigitalSign function.
old-location: security\cryptuiwizfreedigitalsigncontext.htm
old-project: seccrypto
ms.assetid: 039615ee-0485-4698-944f-23359253767a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptUIWizFreeDigitalSignContext, CryptUIWizFreeDigitalSignContext function [Security], cryptuiapi/CryptUIWizFreeDigitalSignContext, security.cryptuiwizfreedigitalsigncontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cryptuiapi.h
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
tech.root: 
req.typenames: CTL_MODIFY_REQUEST, *PCTL_MODIFY_REQUEST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
api_name:
 - CryptUIWizFreeDigitalSignContext
product: Windows
targetos: Windows
req.lib: Cryptui.lib
req.dll: Cryptui.dll
req.irql: 
---

# CryptUIWizFreeDigitalSignContext function


## -description


The <b>CryptUIWizFreeDigitalSignContext</b> function frees the <a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure allocated by the <a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a> function.


## -parameters




### -param pSignContext [in]

A pointer to the   <a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure to be freed.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3e4eb745-0c28-4ce5-870b-d24565ef0cae">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a>



<a href="https://msdn.microsoft.com/1d01523e-d47b-49be-82c8-5e98f97be800">CryptUIWizDigitalSign</a>
 

 

