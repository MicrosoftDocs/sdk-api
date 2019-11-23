---
UID: NF:ktmw32.SetEnlistmentRecoveryInformation
title: SetEnlistmentRecoveryInformation function (ktmw32.h)

description: Sets an opaque, user-defined structure of recovery data from KTM.
old-location: fs\setenlistmentrecoveryinformation.htm
tech.root: ktm
ms.assetid: 54e7526f-57f0-40cd-9624-fce0644a0884

ms.date: 12/05/2018
ms.keywords: SetEnlistmentRecoveryInformation, SetEnlistmentRecoveryInformation function [Files], fs.setenlistmentrecoveryinformation, ktmw32/SetEnlistmentRecoveryInformation
ms.topic: function
f1_keywords: 
 - "ktmw32/SetEnlistmentRecoveryInformation"
dev_langs:
 - c++
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
 - SetEnlistmentRecoveryInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetEnlistmentRecoveryInformation function


## -description


 Sets an opaque, user-defined structure of recovery data from KTM.  Recovery information is stored in a log on behalf of a resource manager (RM) by calling <b>SetEnlistmentRecoveryInformation</b>.  After a failure, the RM can use <a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getenlistmentrecoveryinformation">GetEnlistmentRecoveryInformation</a> to retrieve the information.  


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param BufferSize [in]

The size of <i>Buffer</i>, in bytes.


### -param Buffer [in]

The recovery information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



This call cannot be used with volatile transaction managers.

The information that is provided by the user may not be durably stored in the log at the completion of this operation, but it will be durably stored by the end of the next commit operation for this enlistment.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getenlistmentrecoveryinformation">GetEnlistmentRecoveryInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>
 

 

