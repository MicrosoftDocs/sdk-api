---
UID: NF:ktmw32.OpenResourceManager
title: OpenResourceManager function (ktmw32.h)
description: Opens an existing resource manager (RM).
old-location: fs\openresourcemanager.htm
tech.root: ktm
ms.assetid: 396b586f-c594-4481-b095-862e9058519c
ms.date: 12/05/2018
ms.keywords: OpenResourceManager, OpenResourceManager function [Files], fs.openresourcemanager, ktmw32/OpenResourceManager
ms.topic: function
f1_keywords:
- ktmw32/OpenResourceManager
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
- OpenResourceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenResourceManager function


## -description


Opens an existing resource manager (RM).


## -parameters




### -param dwDesiredAccess [in]

The access requested for the RM. See <a href="https://docs.microsoft.com/windows/desktop/Ktm/resource-manager-access-masks">Resource Manager Access Masks</a> for a list of valid values.


### -param TmHandle [in]

A handle to the transaction manager.


### -param ResourceManagerId [in]

The identifier  for this resource manager.


## -returns



If the function succeeds, the return value is a handle to the resource manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:




## -remarks



Immediately after calling this function, you must call <a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-recoverresourcemanager">RecoverResourceManager</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createresourcemanager">CreateResourceManager</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/resource-manager-access-masks">Resource Manager Access Masks</a>
 

 

