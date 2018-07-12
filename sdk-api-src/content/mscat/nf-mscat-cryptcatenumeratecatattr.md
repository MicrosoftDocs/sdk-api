---
UID: NF:mscat.CryptCATEnumerateCatAttr
title: CryptCATEnumerateCatAttr function
author: windows-sdk-content
description: Enumerates the attributes associated with a catalog. This function has no associated import library.
old-location: security\cryptcatenumeratecatattr.htm
old-project: seccrypto
ms.assetid: 57b6ff5c-e47e-41ac-8ec8-01a47ea77acf
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CryptCATEnumerateCatAttr, CryptCATEnumerateCatAttr function [Security], mscat/CryptCATEnumerateCatAttr, security.cryptcatenumeratecatattr
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
 - CryptCATEnumerateCatAttr
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATEnumerateCatAttr function


## -description


<p class="CCE_Message">[The <b>CryptCATEnumerateCatAttr</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateCatAttr</b> function enumerates the attributes associated with  a catalog. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatalog [in]

Handle for the catalog whose attributes are being enumerated. This value cannot be <b>NULL</b>.


### -param pPrevAttr [in]

A pointer to the previously returned pointer to  the <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure from this function or pointer to <b>NULL</b> to start the enumeration.


## -returns



The return value is a pointer to the  <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure that contains the attribute information or <b>NULL</b>, if no more attributes are in the enumeration or if an error is encountered. The returned pointer is passed in as the <i>pPrevAttr</i> parameter for subsequent calls to this function.




## -remarks



Do not free the returned pointer nor any of the members pointed to by the returned pointer. 




## -see-also




<a href="https://msdn.microsoft.com/064e87db-4330-4b8b-9865-ba8b9714f6e4">CryptCATEnumerateAttr</a>
 

 

