---
UID: NF:mscat.CryptCATAdminAcquireContext
title: CryptCATAdminAcquireContext function
author: windows-sdk-content
description: Acquires a handle to a catalog administrator context.
old-location: security\cryptcatadminacquirecontext.htm
tech.root: seccrypto
ms.assetid: 693af055-fa93-4526-aa9c-3a659f8ff78f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CryptCATAdminAcquireContext, CryptCATAdminAcquireContext function [Security], mscat/CryptCATAdminAcquireContext, security.cryptcatadminacquirecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminAcquireContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATAdminAcquireContext function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminAcquireContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminAcquireContext</b> function acquires a handle to a catalog administrator context. This handle can be used by subsequent calls to the <a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>,  <a href="https://msdn.microsoft.com/33ab2d01-94ab-4d23-a054-9da0731485d6">CryptCATAdminEnumCatalogFromHash</a>, and <a href="https://msdn.microsoft.com/e09fe991-0e7a-45da-910a-8cb148bdff9a">CryptCATAdminRemoveCatalog</a> functions. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param phCatAdmin [out]

A pointer to the catalog administrator context handle that is assigned by this function. When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/dff253dc-c444-46be-a383-41340d634cce">CryptCATAdminReleaseContext</a> function.


### -param pgSubsystem [in]

A pointer to the GUID that identifies the subsystem. DRIVER_ACTION_VERIFY represents the subsystem for operating system components and third party drivers. This is the subsystem used by most implementations.


### -param dwFlags [in]

Not used; set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>



<a href="https://msdn.microsoft.com/dff253dc-c444-46be-a383-41340d634cce">CryptCATAdminReleaseContext</a>



<a href="https://msdn.microsoft.com/e09fe991-0e7a-45da-910a-8cb148bdff9a">CryptCATAdminRemoveCatalog</a>
 

 

