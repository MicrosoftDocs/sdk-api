---
UID: NF:ncrypt.NCryptIsKeyHandle
title: NCryptIsKeyHandle function (ncrypt.h)
author: windows-sdk-content
description: Determines if the specified handle is a CNG key handle.
old-location: security\ncryptiskeyhandle.htm
tech.root: SecCNG
ms.assetid: ad841c2e-8097-4b07-914e-8e7240d55585
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NCryptIsKeyHandle, NCryptIsKeyHandle function [Security], ncrypt/NCryptIsKeyHandle, security.ncryptiskeyhandle
ms.topic: function
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptIsKeyHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptIsKeyHandle function


## -description


The <b>NCryptIsKeyHandle</b> function determines if the specified handle is a CNG key handle.


## -parameters




### -param hKey [in]

The handle of the key to test.


## -returns



Returns a nonzero value if the handle is a key handle or zero otherwise.




## -remarks



A service must not call this function from its <a href="http://go.microsoft.com/fwlink/p/?linkid=137250">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.



