---
UID: NF:mssip.CryptSIPAddProvider
title: CryptSIPAddProvider function
author: windows-sdk-content
description: The CryptSIPAddProvider function registers functions that are exported by a given DLL file that implements a Subject Interface Package (SIP).
old-location: security\cryptsipaddprovider.htm
tech.root: seccrypto
ms.assetid: 99633c2f-e5ed-49e4-9c98-7501f66e5571
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CryptSIPAddProvider, CryptSIPAddProvider function [Security], mssip/CryptSIPAddProvider, security.cryptsipaddprovider
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
 - CryptSIPAddProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSIPAddProvider function


## -description


The <b>CryptSIPAddProvider</b> function registers functions that are exported by a given DLL file that implements  a Subject Interface Package (SIP).


## -parameters




### -param psNewProv [in]

A pointer to a <a href="https://msdn.microsoft.com/5ca88c0c-a7c9-4517-a874-49d38c1bc7c3">SIP_ADD_NEWPROVIDER</a> structure that specifies the DLL file and function names to register.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to determine the reason for failure.




## -remarks



Typically, you call this function as part of an in-process COM server registration. The <b>CryptSIPAddProvider</b> function persists the appropriate Registry entries for the SIP provider functions.

When you have finished using the added SIP provider, remove it by calling the <a href="https://msdn.microsoft.com/0a269956-b2c7-414a-b002-7cec0d52bfd6">CryptSIPRemoveProvider</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0a269956-b2c7-414a-b002-7cec0d52bfd6">CryptSIPRemoveProvider</a>
 

 

