---
UID: NS:ntquery.tagCIPROPERTYDEF
title: tagCIPROPERTYDEF
author: windows-driver-content
description: Represents the friendly name, type, and property identifier (ID) information.
old-location: indexsrv\cipropertydef.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0ucm.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CIPROPERTYDEF, CIPROPERTYDEF structure [Indexing Service], _idxs_CIPROPERTYDEF, indexsrv.cipropertydef, ntquery/CIPROPERTYDEF, tagCIPROPERTYDEF
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CIPROPERTYDEF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntquery.h
api_name:
-	CIPROPERTYDEF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# tagCIPROPERTYDEF structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Represents the friendly name, type, and property identifier (ID) information.


## -struct-fields




### -field wcsFriendlyName

The friendly name for a property. The friendly name can be used in an Indexing Service query, column list, or sort order parsed by the <a href="https://msdn.microsoft.com/333fb241-f484-4d79-89cd-9b1d8240b8a8">CITextToSelectTree</a> function and the <a href="https://msdn.microsoft.com/679b96f7-43b3-44c1-86dd-e995bb9a9c53">CITextToFullTree</a> function. Friendly names must be entered in uppercase.


### -field dbType

The data type for the property. This type is used when building a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure for a restriction node. The same property with different friendly names can have different types. Its value must be either an OLE DB <b>DBTYPE</b> type or a <b>PROPVARIANT</b> variant type.


### -field dbCol

The property ID for the property. Indexing Service properties must be either DBKIND_GUID_NAME or DBKIND_GUID_PROPID. See <a href="https://msdn.microsoft.com/076f4603-8621-4c32-b4d7-cf8507d240a8">DBID</a>.


## -see-also




<a href="https://msdn.microsoft.com/679b96f7-43b3-44c1-86dd-e995bb9a9c53">CITextToFullTree</a>



<a href="https://msdn.microsoft.com/333fb241-f484-4d79-89cd-9b1d8240b8a8">CITextToSelectTree</a>



<a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a>



<a href="https://msdn.microsoft.com/076f4603-8621-4c32-b4d7-cf8507d240a8">DBID</a>
 

 

