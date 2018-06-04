---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CryptSIPLoad function


## -description


The <b>CryptSIPLoad</b> function loads the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">dynamic-link library</a> (DLL) that implements a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) and assigns appropriate library export functions to a <a href="https://msdn.microsoft.com/d34b5081-0af8-4dcc-8133-a91d0603d419">SIP_DISPATCH_INFO</a> structure. The exported functions must have been previously registered by calling the <a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a> function.


## -parameters




### -param pgSubject [in]

A pointer to a GUID returned by calling the <a href="https://msdn.microsoft.com/b81472bc-6d9c-4634-a378-e39786a0ca09">CryptSIPRetrieveSubjectGuid</a> function.


### -param dwFlags [in]

This parameter is reserved and must be set to zero.


### -param pSipDispatch [in, out]

A pointer to a <a href="https://msdn.microsoft.com/d34b5081-0af8-4dcc-8133-a91d0603d419">SIP_DISPATCH_INFO</a> structure that contains pointers to SIP provider functions that are specific to the subject type. The caller must initialize this structure to binary zeros, and set the <b>cbSize</b> member to <code>sizeof(SIP_DISPATCH_INFO)</code> before calling the <b>CryptSIPLoad</b> function.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



