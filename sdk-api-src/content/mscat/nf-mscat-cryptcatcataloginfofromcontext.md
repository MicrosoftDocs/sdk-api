---
UID: NF:mscat.CryptCATCatalogInfoFromContext
title: CryptCATCatalogInfoFromContext function
author: windows-sdk-content
description: Retrieves catalog information from a specified catalog context.
old-location: security\cryptcatcataloginfofromcontext.htm
old-project: seccrypto
ms.assetid: ec195fcc-1cff-4dd6-9075-c4904b653da7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CryptCATCatalogInfoFromContext, CryptCATCatalogInfoFromContext function [Security], mscat/CryptCATCatalogInfoFromContext, security.cryptcatcataloginfofromcontext
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
 - CryptCATCatalogInfoFromContext
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATCatalogInfoFromContext function


## -description


<p class="CCE_Message">[The <b>CryptCATCatalogInfoFromContext</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATCatalogInfoFromContext</b> function retrieves catalog information from a specified catalog context. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatInfo [in]

A handle to the catalog context. This value cannot be <b>NULL</b>.


### -param psCatInfo [in, out]

A pointer to the <a href="https://msdn.microsoft.com/f6e66412-3ed2-48d9-a377-5df11500db59">CATALOG_INFO</a> structure. This value cannot be <b>NULL</b>. Upon return from this function, the <i>wszCatalogFile</i> member of the CATALOG_INFO structure contains the catalog file name.


### -param dwFlags [in]

Unused; set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.

For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. For a complete list of error codes provided by the operating system, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



