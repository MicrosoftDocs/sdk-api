---
UID: NF:ktmw32.RenameTransactionManager
title: RenameTransactionManager function
author: windows-sdk-content
description: Renames a transaction manager (TM) object. This function can only be used on named TM handles.
old-location: fs\renametransactionmanager.htm
tech.root: ktm
ms.assetid: 2767e689-1342-458f-a215-a29d774c0648
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RenameTransactionManager, RenameTransactionManager function [Files], fs.renametransactionmanager, ktmw32/RenameTransactionManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - RenameTransactionManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RenameTransactionManager function


## -description


Renames a transaction manager (TM) object. This function can only be used on named TM 
    handles. A new <b>GUID</b> for the TM is selected and can be retrieved using the 
    <a href="https://msdn.microsoft.com/e1aa573d-add9-42b7-8b2b-773dc12aa51b">GetTransactionManagerID</a> function.


## -parameters




### -param LogFileName [in]

The name of the log stream.  This stream must exist within a CLFS log file.


### -param ExistingTransactionManagerGuid [in]

A value that specifies the current name of the TM.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/e1aa573d-add9-42b7-8b2b-773dc12aa51b">GetTransactionManagerID</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

