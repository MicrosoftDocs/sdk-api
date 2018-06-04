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

# CryptUninstallDefaultContext function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>
			The <b>CryptUninstallDefaultContext</b> function removes a default <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a> previously installed by <a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a>. This function will block until any threads currently using this context finish, if the default context was installed with CRYPT_DEFAULT_CONTEXT_PROCESS_FLAG set.


## -parameters




### -param hDefaultContext [in]

Handle of the context to be released.


### -param dwFlags [in]

Reserved for future use.


### -param pvReserved [in]

Reserved for future use.


## -returns




						If the function succeeds, the return value is nonzero (TRUE) .If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



