---
UID: NF:ktmw32.GetTransactionInformation
title: GetTransactionInformation function
author: windows-sdk-content
description: Returns the requested information about the specified transaction.
old-location: fs\gettransactioninformation_func.htm
tech.root: Ktm
ms.assetid: 5ce3c96a-629e-49d0-8ec4-f9bf76af99ac
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTransactionInformation, GetTransactionInformation function [Files], fs.gettransactioninformation_func, ktmw32/GetTransactionInformation
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
 - GetTransactionInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTransactionInformation function


## -description


Returns the requested information about the specified transaction.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction. The handle must have  the TRANSACTION_QUERY_INFORMATION permission to retrieve the information.


### -param Outcome [out, optional]

A pointer to a buffer that receives the current outcome of the transaction. If the call to the <b>GetTransactionInformation</b> function is successful, this value will be one of the <a href="https://msdn.microsoft.com/d4315a62-b65f-4744-8084-2317ad39c32c">TRANSACTION_OUTCOME</a> enumeration values.


### -param IsolationLevel [out, optional]

Reserved.


### -param IsolationFlags [out, optional]

Reserved.


### -param Timeout [out, optional]

A pointer to a variable that receives the timeout value, in milliseconds, for this transaction.


### -param BufferLength [in]

The size of the <i>Description</i> parameter, in bytes. The buffer length value cannot be longer than the value of MAX_TRANSACTION_DESCRIPTION_LENGTH.


### -param Description [out, optional]

A pointer to a buffer that receives the user-defined description of the transaction.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/e33d221b-cd06-4f20-a4b5-407a04362ba0">SetTransactionInformation</a>
 

 

