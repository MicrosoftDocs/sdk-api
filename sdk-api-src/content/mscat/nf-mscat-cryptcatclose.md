---
UID: NF:mscat.CryptCATClose
title: CryptCATClose function
author: windows-driver-content
description: Closes a catalog handle opened previously by the CryptCATOpen function.
old-location: security\cryptcatclose.htm
old-project: SecCrypto
ms.assetid: f6fa2d10-0049-4d5e-9688-566e5c11d64e
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CryptCATClose, CryptCATClose function [Security], mscat/CryptCATClose, security.cryptcatclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mscat.h
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
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wintrust.dll
api_name:
-	CryptCATClose
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATClose function


## -description


<p class="CCE_Message">[The <b>CryptCATClose</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATClose</b> function closes a catalog handle opened previously by the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatalog [in]

Handle opened previously by a call to the  <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> function.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a>
 

 

