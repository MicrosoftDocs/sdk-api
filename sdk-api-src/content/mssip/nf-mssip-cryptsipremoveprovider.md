---
UID: NF:mssip.CryptSIPRemoveProvider
title: CryptSIPRemoveProvider function
author: windows-sdk-content
description: Removes registry details of a Subject Interface Package (SIP) DLL file added by a previous call to the CryptSIPAddProvider function.
old-location: security\cryptsipremoveprovider.htm
tech.root: SecCrypto
ms.assetid: 0a269956-b2c7-414a-b002-7cec0d52bfd6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CryptSIPRemoveProvider, CryptSIPRemoveProvider function [Security], mssip/CryptSIPRemoveProvider, security.cryptsipremoveprovider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mssip.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPRemoveProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSIPRemoveProvider function


## -description


The <b>CryptSIPRemoveProvider</b> function removes registry details of a Subject Interface Package (SIP) DLL file  added by a previous call to the <a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a> function.


## -parameters




### -param pgProv [in]

A pointer to the GUID that identifies the SIP DLL  to remove. 


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to determine the reason for failure.




## -remarks



Typically you call this function to unregister an in-process COM server. The <b>CryptSIPRemoveProvider</b> function removes the appropriate Registry entries for the SIP provider functions.




## -see-also




<a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a>
 

 

