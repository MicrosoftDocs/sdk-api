---
UID: NF:mscat.CryptCATGetMemberInfo
title: CryptCATGetMemberInfo function
author: windows-sdk-content
description: Retrieves member information from the catalog's PKCS #7.
old-location: security\cryptcatgetmemberinfo.htm
old-project: SecCrypto
ms.assetid: ff265232-f57e-4ab0-ba07-05e6d6745ae3
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CryptCATGetMemberInfo, CryptCATGetMemberInfo function [Security], mscat/CryptCATGetMemberInfo, security.cryptcatgetmemberinfo
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
 - CryptCATGetMemberInfo
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATGetMemberInfo function


## -description


<p class="CCE_Message">[The <b>CryptCATGetMemberInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATGetMemberInfo</b> function retrieves member information from the catalog's PKCS #7. In addition to retrieving the member information for a specified reference tag, this function opens a member context. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatalog [in]

A handle to the catalog. This parameter cannot be <b>NULL</b>.


### -param pwszReferenceTag [in]

A pointer to a <b>null</b>-terminated string that represents the reference tag for the member information being retrieved.


## -returns



A pointer to the <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that contains the member information or <b>NULL</b>, if no information can be found.




## -remarks



Do not free the returned pointer nor any of the members pointed to by the returned pointer. 



