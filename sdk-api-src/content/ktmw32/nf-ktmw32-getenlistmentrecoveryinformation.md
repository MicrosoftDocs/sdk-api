---
UID: NF:ktmw32.GetEnlistmentRecoveryInformation
title: GetEnlistmentRecoveryInformation function
author: windows-sdk-content
description: Retrieves an opaque structure of recovery data from KTM.
old-location: fs\getenlistmentrecoveryinformation_func.htm
tech.root: Ktm
ms.assetid: 05bfbe81-5f3d-4e32-b4fa-4532227f522e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetEnlistmentRecoveryInformation, GetEnlistmentRecoveryInformation function [Files], fs.getenlistmentrecoveryinformation_func, ktmw32/GetEnlistmentRecoveryInformation
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
 - GetEnlistmentRecoveryInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetEnlistmentRecoveryInformation
: 
---

# GetEnlistmentRecoveryInformation function


## -description


 Retrieves an opaque structure of recovery data from KTM.  Recovery information is stored in a log on behalf of a resource manager (RM) by calling the <a href="https://msdn.microsoft.com/54e7526f-57f0-40cd-9624-fce0644a0884">SetEnlistmentRecoveryInformation</a> function.  After a failure, the RM can use the <b>GetEnlistmentRecoveryInformation</b> function to retrieve the information.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param BufferSize [in]

The size of the <i>Buffer</i> parameter, in bytes.


### -param Buffer [out]

A pointer to a buffer that receives the enlistment recovery information.


### -param BufferUsed [out, optional]

A pointer to a variable that receives the actual number of bytes returned in the <i>Buffer</i> parameter.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



This call cannot be used with volatile transaction managers.




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/54e7526f-57f0-40cd-9624-fce0644a0884">SetEnlistmentRecoveryInformation</a>
 

 

