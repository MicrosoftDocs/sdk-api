---
UID: NS:ntquery.tagCIPROPERTYDEF
title: CIPROPERTYDEF (ntquery.h)

description: Represents the friendly name, type, and property identifier (ID) information.
old-location: indexsrv\cipropertydef.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0ucm.htm

ms.date: 12/05/2018
ms.keywords: CIPROPERTYDEF, CIPROPERTYDEF structure [Indexing Service], _idxs_CIPROPERTYDEF, indexsrv.cipropertydef, ntquery/CIPROPERTYDEF
ms.topic: struct
f1_keywords: 
 - "ntquery/CIPROPERTYDEF"
dev_langs:
 - c++
req.header: ntquery.h
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
 - Ntquery.h
api_name:
 - CIPROPERTYDEF
targetos: Windows
req.typenames: CIPROPERTYDEF
req.redist: 
ms.custom: 19H1
---

# CIPROPERTYDEF structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Represents the friendly name, type, and property identifier (ID) information.


## -struct-fields




### -field wcsFriendlyName

The friendly name for a property. The friendly name can be used in an Indexing Service query, column list, or sort order parsed by the <a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttree">CITextToSelectTree</a> function and the <a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-citexttofulltree">CITextToFullTree</a> function. Friendly names must be entered in uppercase.


### -field dbType

The data type for the property. This type is used when building a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure for a restriction node. The same property with different friendly names can have different types. Its value must be either an OLE DB <b>DBTYPE</b> type or a <b>PROPVARIANT</b> variant type.


### -field dbCol

The property ID for the property. Indexing Service properties must be either DBKIND_GUID_NAME or DBKIND_GUID_PROPID. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/dbid">DBID</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-citexttofulltree">CITextToFullTree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-citexttoselecttree">CITextToSelectTree</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/dbid">DBID</a>
 

 

