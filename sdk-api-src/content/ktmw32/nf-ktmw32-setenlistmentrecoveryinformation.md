---
UID: NF:ktmw32.SetEnlistmentRecoveryInformation
title: SetEnlistmentRecoveryInformation function
author: windows-sdk-content
description: Sets an opaque, user-defined structure of recovery data from KTM.
old-location: fs\setenlistmentrecoveryinformation.htm
old-project: Ktm
ms.assetid: 54e7526f-57f0-40cd-9624-fce0644a0884
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SetEnlistmentRecoveryInformation, SetEnlistmentRecoveryInformation function [Files], fs.setenlistmentrecoveryinformation, ktmw32/SetEnlistmentRecoveryInformation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - SetEnlistmentRecoveryInformation
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetEnlistmentRecoveryInformation function


## -description


 Sets an opaque, user-defined structure of recovery data from KTM.  Recovery information is stored in a log on behalf of a resource manager (RM) by calling <b>SetEnlistmentRecoveryInformation</b>.  After a failure, the RM can use <a href="https://msdn.microsoft.com/05bfbe81-5f3d-4e32-b4fa-4532227f522e">GetEnlistmentRecoveryInformation</a> to retrieve the information.  


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param BufferSize [in]

The size of <i>Buffer</i>, in bytes.


### -param Buffer [in]

The recovery information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



This call cannot be used with volatile transaction managers.

The information that is provided by the user may not be durably stored in the log at the completion of this operation, but it will be durably stored by the end of the next commit operation for this enlistment.




## -see-also




<a href="https://msdn.microsoft.com/05bfbe81-5f3d-4e32-b4fa-4532227f522e">GetEnlistmentRecoveryInformation</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

