---
UID: NF:searchapi.ISearchQueryHelper.WriteProperties
title: ISearchQueryHelper::WriteProperties
author: windows-sdk-content
description: Not implemented.
old-location: search\_search_ISearchQueryHelper_WriteProperties.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\writeproperties.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper interface [search],WriteProperties method, ISearchQueryHelper.WriteProperties, ISearchQueryHelper::WriteProperties, WriteProperties, WriteProperties method [search], WriteProperties method [search],ISearchQueryHelper interface, _search_ISearchQueryHelper_WriteProperties, search._search_ISearchQueryHelper_WriteProperties, searchapi/ISearchQueryHelper::WriteProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: Searchapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
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
 - COM
api_location:
 - searchapi.h
api_name:
 - ISearchQueryHelper.WriteProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchQueryHelper::WriteProperties


## -description


Not implemented.


## -parameters




### -param itemID [in]

Type: <b>int</b>

The ItemID that is to be affected. The ItemID is used to store the items unique identifier, such as a DocID.


### -param dwNumberOfColumns [in]

Type: <b>DWORD</b>

The number of properties being written.


### -param pColumns [in]

Type: <b><a href="_shell_PROPERTYKEY">PROPERTYKEY</a>*</b>

 
                Pointer to an array of <a href="_shell_PROPERTYKEY">PROPERTYKEY</a> structures that represent the properties.


### -param pValues [in]

Type: <b><a href="https://msdn.microsoft.com/89a3c625-7853-4e4d-8fb7-dd0a1c998ead">SEARCH_COLUMN_PROPERTIES</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/89a3c625-7853-4e4d-8fb7-dd0a1c998ead">SEARCH_COLUMN_PROPERTIES</a> structures that hold the property values.


### -param pftGatherModifiedTime [in]

Type: <b><a href="_com_FILETIME">FILETIME</a>*</b>

A pointer to the last modified time for the item being written. This time stamp is used later to see if an item has been changed and requires updating.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/75d4882c-305a-4035-9c8c-e72de3c6812f">ISearchQueryHelper::put_QueryContentProperties</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>



<a href="http://msdn.microsoft.com/en-us/library/ff518152(v=VS.85).aspx">System Properties</a>
 

 

