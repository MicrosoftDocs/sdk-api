---
UID: NS:oledbguid.tagDBID
title: DBID
author: windows-sdk-content
description: The DBID structure encapsulates various ways of identifying a database object.
old-location: indexsrv\dbid.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_4bhg.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DBID, DBID structure [Indexing Service], _idxs_DBID, indexsrv.dbid, oledbguid/DBID, tagDBID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: oledbguid.h
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
 - oledbguid.h
api_name:
 - DBID
product: Windows
targetos: Windows
req.typenames: DBID
req.redist: 
---

# DBID structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBID</b> structure encapsulates various ways of identifying a database object. It is used by nodes that must represent a column name, such as column_name, index_name, table_name, schema_name, catalog_name, and so forth. (For more information on these nodes, see <a href="https://msdn.microsoft.com/en-us/library/ms689915(v=VS.85).aspx">Catalog of DML Nodes</a>.) This structure is also used to define bindings.


## -struct-fields




### -field uGuid


### -field uGuid.guid

 


### -field uGuid.pguid

 


### -field eKind


### -field uName


### -field uName.pwszName

 


### -field uName.ulPropid

 




## -remarks



The <b>DBID</b> structure identifies the requested columns for a query. Each unique column is represented by a unique combination of GUID and number or GUID and name.



