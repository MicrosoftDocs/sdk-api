---
UID: NF:ktmw32.GetEnlistmentRecoveryInformation
title: GetEnlistmentRecoveryInformation function (ktmw32.h)
description: Retrieves an opaque structure of recovery data from KTM.
helpviewer_keywords: ["GetEnlistmentRecoveryInformation","GetEnlistmentRecoveryInformation function [Files]","fs.getenlistmentrecoveryinformation_func","ktmw32/GetEnlistmentRecoveryInformation"]
old-location: fs\getenlistmentrecoveryinformation_func.htm
tech.root: fs
ms.assetid: 05bfbe81-5f3d-4e32-b4fa-4532227f522e
ms.date: 12/05/2018
ms.keywords: GetEnlistmentRecoveryInformation, GetEnlistmentRecoveryInformation function [Files], fs.getenlistmentrecoveryinformation_func, ktmw32/GetEnlistmentRecoveryInformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEnlistmentRecoveryInformation
 - ktmw32/GetEnlistmentRecoveryInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - GetEnlistmentRecoveryInformation
---

# GetEnlistmentRecoveryInformation function


## -description

 Retrieves an opaque structure of recovery data from KTM.  Recovery information is stored in a log on behalf of a resource manager (RM) by calling the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-setenlistmentrecoveryinformation">SetEnlistmentRecoveryInformation</a> function.  After a failure, the RM can use the <b>GetEnlistmentRecoveryInformation</b> function to retrieve the information.

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

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -remarks

This call cannot be used with volatile transaction managers.

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-setenlistmentrecoveryinformation">SetEnlistmentRecoveryInformation</a>