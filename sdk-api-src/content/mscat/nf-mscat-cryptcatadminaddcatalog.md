---
UID: NF:mscat.CryptCATAdminAddCatalog
title: CryptCATAdminAddCatalog function
author: windows-sdk-content
description: Adds a catalog to the catalog database.
old-location: security\cryptcatadminaddcatalog.htm
old-project: seccrypto
ms.assetid: a227597c-a0af-4b86-bd29-03f478aef244
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CryptCATAdminAddCatalog, CryptCATAdminAddCatalog function [Security], mscat/CryptCATAdminAddCatalog, security.cryptcatadminaddcatalog
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminAddCatalog
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATAdminAddCatalog function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminAddCatalog</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminAddCatalog</b> function adds a catalog to the catalog database. The catalog database is an index that associates file hashes with the catalogs that contain them.  It is used to speed the identification of the catalogs when verifying the file signature.  This function is the only supported way to programmatically add catalogs to the Windows catalog database. The function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle previously assigned by the  <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param pwszCatalogFile [in]

A pointer to a <b>null</b>-terminated string for the fully qualified path of the catalog to be added.


### -param pwszSelectBaseName [in]

A pointer to a <b>null</b>-terminated string for the name of the catalog when it is stored. If the parameter is <b>NULL</b>, then a unique name will be generated for the catalog.


### -param dwFlags [in]

If the CRYPTCAT_ADDCATALOG_HARDLINK (0x00000001) flag is specified, the catalog specified in the call will be hard-linked to rather than copied. Hard-linking instead of copying a catalog reduces the amount of disk space required by Windows.


## -returns



If the function succeeds, the return value is a handle to the catalog information context. If the function fails, the return value is <b>NULL</b>. After you have finished using the returned handle, free it by calling the  <a href="https://msdn.microsoft.com/6cc13013-2c0a-4934-a866-30b69cbcf934">CryptCATAdminReleaseCatalogContext</a> function.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a>



<a href="https://msdn.microsoft.com/6cc13013-2c0a-4934-a866-30b69cbcf934">CryptCATAdminReleaseCatalogContext</a>
 

 

