---
UID: NS:searchapi._ITEM_INFO
title: "_ITEM_INFO"
author: windows-sdk-content
description: Contains information passed to the IUrlAccessor object about the current item; for example, the application name and catalog name.
old-location: search\_search_ITEM_INFO.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\item_info.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITEM_INFO, ITEM_INFO structure [search], _ITEM_INFO, _search_ITEM_INFO, search._search_ITEM_INFO, searchapi/ITEM_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - ITEM_INFO
product: Windows
targetos: Windows
req.typenames: ITEM_INFO
req.redist: Windows Desktop Search (WDS) 3.0
---

# _ITEM_INFO structure


## -description


Contains information passed to the <a href="https://msdn.microsoft.com/en-us/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object about the current item; for example, the application name and catalog name.


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

