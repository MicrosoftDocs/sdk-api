---
UID: NS:cmdtree.tagDBSORTINFO
title: tagDBSORTINFO
author: windows-sdk-content
description: The DBSORTINFO structure stores the order in which a column will be sorted (that is, ascending or descending). This information is stored inside a DBOP_sort_list_element node.
old-location: indexsrv\dbsortinfo.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2mpb.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DBSORTINFO, DBSORTINFO structure [Indexing Service], _idxs_DBSORTINFO, cmdtree/DBSORTINFO, indexsrv.dbsortinfo, tagDBSORTINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - cmdtree.h
api_name:
 - DBSORTINFO
product: Windows
targetos: Windows
req.typenames: DBSORTINFO
req.redist: 
---

# tagDBSORTINFO structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBSORTINFO</b> structure stores the order in which a column will be sorted (that is, ascending or descending). This information is stored inside a DBOP_sort_list_element node.


## -struct-fields




### -field fDesc

TRUE = ascending, FALSE = descending


### -field lcid

locale identifier


## -remarks



The locale identifier (LCID) specifies a set of user preference information related to the user's language. It determines how times are formatted, how items are alphabetically sorted, and how strings are compared.

For additional information on LCIDs see <a href="_win32_locales">Locales</a>.



