---
UID: NF:ktmw32.GetTransactionId
title: GetTransactionId function
author: windows-sdk-content
description: Obtains the identifier (ID) for the specified transaction.
old-location: fs\gettransactionid.htm
tech.root: ktm
ms.assetid: 10f4729f-3e6e-469a-8f72-48c29735e7b1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTransactionId, GetTransactionId function [Files], fs.gettransactionid, ktmw32/GetTransactionId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - GetTransactionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTransactionId function


## -description


Obtains the identifier (ID) for the specified transaction.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction.


### -param TransactionId [out]

A pointer to a variable that receives the ID of the transaction.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

