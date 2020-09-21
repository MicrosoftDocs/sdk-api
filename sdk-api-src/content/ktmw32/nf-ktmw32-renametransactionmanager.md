---
UID: NF:ktmw32.RenameTransactionManager
title: RenameTransactionManager function (ktmw32.h)
description: Renames a transaction manager (TM) object. This function can only be used on named TM handles.
helpviewer_keywords: ["RenameTransactionManager","RenameTransactionManager function [Files]","fs.renametransactionmanager","ktmw32/RenameTransactionManager"]
old-location: fs\renametransactionmanager.htm
tech.root: fs
ms.assetid: 2767e689-1342-458f-a215-a29d774c0648
ms.date: 12/05/2018
ms.keywords: RenameTransactionManager, RenameTransactionManager function [Files], fs.renametransactionmanager, ktmw32/RenameTransactionManager
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RenameTransactionManager
 - ktmw32/RenameTransactionManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - RenameTransactionManager
---

# RenameTransactionManager function


## -description

Renames a transaction manager (TM) object. This function can only be used on named TM 
    handles. A new <b>GUID</b> for the TM is selected and can be retrieved using the 
    <a href="/windows/desktop/api/ktmw32/nf-ktmw32-gettransactionmanagerid">GetTransactionManagerID</a> function.

## -parameters

### -param LogFileName [in]

The name of the log stream.  This stream must exist within a CLFS log file.

### -param ExistingTransactionManagerGuid [in]

A value that specifies the current name of the TM.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-gettransactionmanagerid">GetTransactionManagerID</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>