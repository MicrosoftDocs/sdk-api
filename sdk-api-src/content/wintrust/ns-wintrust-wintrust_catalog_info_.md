---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WINTRUST_CATALOG_INFO_ structure


## -description



			The <b>WINTRUST_CATALOG_INFO</b> structure is used when calling 
<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a> to verify a member of a Microsoft catalog.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field dwCatalogVersion

Optional. Catalog version number.


### -field pcwszCatalogFilePath

The full path and file name of the catalog file that contains the member to be verified.


### -field pcwszMemberTag

Tag of a member file to be verified.


### -field pcwszMemberFilePath

The full path and file name of the catalog member file to be verified.


### -field hMemberFile

Optional. Handle of the open catalog member file to be verified. The handle must be to a file with at least read permissions.


### -field pbCalculatedFileHash

Optional. The calculated hash of the file that contains the file to be verified.


### -field cbCalculatedFileHash

The size, in bytes, of the value passed in the <b>pbCalculatedFileHash</b> member. <b>cbCalculatedFileHash</b> is used only if the calculated hash is being passed.


### -field pcCatalogContext

A pointer to a <a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure that represents  a catalog context to be used instead of a catalog file.


### -field hCatAdmin

Handle to the catalog administrator context that was used when calculating the hash of the file. This value can be zero only for a SHA1 file hash.<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.



