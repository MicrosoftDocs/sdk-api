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

# _ITEM_INFO structure


## -description


Contains information passed to the <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object about the current item; for example, the application name and catalog name.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

Size of the structure in bytes.


### -field pcwszFromEMail

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing an email address that is notified in case of error.


### -field pcwszApplicationName

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the application name.


### -field pcwszCatalogName

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the workspace name from which the crawl to this content source was initiated.


### -field pcwszContentClass

Type: <b>LPCWSTR</b>

Not used by protocol handlers.

