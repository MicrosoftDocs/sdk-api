---
UID: NF:ktmw32.OpenEnlistment
title: OpenEnlistment function
author: windows-sdk-content
description: Opens an existing enlistment object, and returns a handle to the enlistment.
old-location: fs\openenlistment.htm
tech.root: Ktm
ms.assetid: 2c403e22-3feb-415a-b65b-572802764548
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OpenEnlistment, OpenEnlistment function [Files], fs.openenlistment, ktmw32/OpenEnlistment
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
 - OpenEnlistment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OpenEnlistment
: 
---

# OpenEnlistment function


## -description


Opens an existing enlistment object, and returns a handle to the enlistment.


## -parameters




### -param dwDesiredAccess [in]

The access requested for this enlistment. See <a href="https://msdn.microsoft.com/93773eb7-141a-49f3-9306-ffbda2f4ab9f">Enlistment Access Masks</a> for a list of valid values.


### -param ResourceManagerHandle [in]

A handle to the resource manager.


### -param EnlistmentId [in]

The enlistment identifier.


## -returns



If the function succeeds, the return value is a handle to the enlistment.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/7bc06468-947f-48ec-8e58-20df58ed93bd">CreateEnlistment</a>



<a href="https://msdn.microsoft.com/93773eb7-141a-49f3-9306-ffbda2f4ab9f">Enlistment Access Masks</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

