---
UID: NF:ktmw32.GetEnlistmentId
title: GetEnlistmentId function (ktmw32.h)
author: windows-sdk-content
description: Obtains the identifier (ID) for the specified enlistment.
old-location: fs\getenlistmentid.htm
tech.root: ktm
ms.assetid: ffd37a2e-6bac-4566-bb15-eafce8a11c3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEnlistmentId, GetEnlistmentId function [Files], fs.getenlistmentid, ktmw32/GetEnlistmentId
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
 - GetEnlistmentId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetEnlistmentId function


## -description


Obtains the identifier (ID) for the specified enlistment.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param EnlistmentId [out]

A pointer to a variables that receives the ID of the enlistment.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>
 

 

