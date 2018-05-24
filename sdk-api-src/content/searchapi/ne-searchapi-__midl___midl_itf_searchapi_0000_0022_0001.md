---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0022_0001
title: "__MIDL___MIDL_itf_searchapi_0000_0022_0001"
author: windows-driver-content
description: Used by the IRowsetPrioritization interface to sets or retrieve the current indexer prioritization level for the scope specified by a query.
old-location: search\_search_PRIORITY_LEVEL.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\priority_level.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: PRIORITY_LEVEL, PRIORITY_LEVEL enumeration [search], PRIORITY_LEVEL_DEFAULT, PRIORITY_LEVEL_FOREGROUND, PRIORITY_LEVEL_HIGH, PRIORITY_LEVEL_LOW, __MIDL___MIDL_itf_searchapi_0000_0022_0001, _search_PRIORITY_LEVEL, search._search_PRIORITY_LEVEL, searchapi/PRIORITY_LEVEL, searchapi/PRIORITY_LEVEL_DEFAULT, searchapi/PRIORITY_LEVEL_FOREGROUND, searchapi/PRIORITY_LEVEL_HIGH, searchapi/PRIORITY_LEVEL_LOW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	PRIORITY_LEVEL
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_searchapi_0000_0022_0001 enumeration


## -description


Used by the <a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a> interface to sets or retrieve the current indexer prioritization level for the scope specified by a query.


## -enum-fields




### -field PRIORITY_LEVEL_FOREGROUND

Indicates that the indexer should process items as fast as the machine allows.


### -field PRIORITY_LEVEL_HIGH

Indicates that the indexer should process items in this scope first, and as quickly as possible.


### -field PRIORITY_LEVEL_LOW

Indicates that the indexer should process items in this scope before those at the normal rate, but after any other prioritization requests.


### -field PRIORITY_LEVEL_DEFAULT

Indicates that the indexer should  process items at the normal indexer rate.


## -remarks



The SearchEvents code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to prioritize indexing events.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82dce1fa-9bc5-4744-966e-1e7aa6fc3e05">IRowsetPrioritization</a>



<a href="https://msdn.microsoft.com/6cdfb7d3-f849-432c-960f-912e5024c583">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://msdn.microsoft.com/554d405e-c117-4597-9612-20cd6088ebef">PRIORITIZE_FLAGS</a>



<a href="https://msdn.microsoft.com/2df331c6-9048-4720-b582-0025461134c1">ROWSETEVENT_ITEMSTATE</a>



<a href="https://msdn.microsoft.com/c9fb74f6-8aed-4450-9bc4-d9f5c3e835a4">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71aa0ad6-ef34-47ee-945f-04bda20bf8a4">Rowset Properties</a>
 

 

