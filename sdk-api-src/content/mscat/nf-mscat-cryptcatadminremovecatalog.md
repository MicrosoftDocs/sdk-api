---
UID: NF:mscat.CryptCATAdminRemoveCatalog
title: CryptCATAdminRemoveCatalog function
author: windows-sdk-content
description: Deletes a catalog file and removes that catalog's entry from the Windows catalog database.
old-location: security\cryptcatadminremovecatalog.htm
tech.root: seccrypto
ms.assetid: e09fe991-0e7a-45da-910a-8cb148bdff9a
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CryptCATAdminRemoveCatalog, CryptCATAdminRemoveCatalog function [Security], mscat/CryptCATAdminRemoveCatalog, security.cryptcatadminremovecatalog
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
 - CryptCATAdminRemoveCatalog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATAdminRemoveCatalog function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminRemoveCatalog</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminRemoveCatalog</b> function deletes a catalog file and removes that catalog's entry from the Windows catalog database. This function is the only supported way to remove catalogs from the database while ensuring the integrity of the database. The function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle previously assigned by the  <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param pwszCatalogFile [in]

A pointer to a null-terminated string for the name of the catalog to remove. This string must contain only the name, without any path information.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>
 

 

