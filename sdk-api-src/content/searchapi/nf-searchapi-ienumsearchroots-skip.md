---
UID: NF:searchapi.IEnumSearchRoots.Skip
title: IEnumSearchRoots::Skip
author: windows-driver-content
description: Skips the specified number of elements.
old-location: search\_search_IEnumSearchRoots_Skip.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\ienumsearchroots\skip.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IEnumSearchRoots interface [search],Skip method, IEnumSearchRoots.Skip, IEnumSearchRoots::Skip, Skip, Skip method [search], Skip method [search],IEnumSearchRoots interface, _search_IEnumSearchRoots_Skip, search._search_IEnumSearchRoots_Skip, searchapi/IEnumSearchRoots::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IEnumSearchRoots.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSearchRoots::Skip


## -description



            Skips the specified number of elements.
        


## -parameters




### -param celt [in]

Type: <b>ULONG</b>


                    The number of elements to skip.
                


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there were not enough items left in the enumeration to skip, or an error value.




## -remarks



<b>IEnumSearchRoots::Skip</b> moves the internal counter forward a specified number of elements so that a subsequent call to <a href="https://msdn.microsoft.com/58838414-0609-4da8-9467-1ebfb5e42d8c">IEnumSearchRoots::Next</a> starts from that point. 

<b>Windows 7 and later</b>: the CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.



