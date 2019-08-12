---
UID: NS:filter.tagFULLPROPSPEC
title: FULLPROPSPEC (filter.h)
author: windows-sdk-content
description: Specifies a property set and a property within the property set.
old-location: indexsrv\fullpropspec.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_599f.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FULLPROPSPEC, FULLPROPSPEC structure [Indexing Service], _idxs_FULLPROPSPEC, filter/FULLPROPSPEC, indexsrv.fullpropspec, tagFULLPROPSPEC
ms.topic: struct
f1_keywords: 
 - "filter/FULLPROPSPEC"
req.header: filter.h
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
 - Filter.h
api_name:
 - FULLPROPSPEC
product: Windows
targetos: Windows
req.typenames: FULLPROPSPEC
req.redist: 
ms.custom: 19H1
---

# FULLPROPSPEC structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies a property set and a property within the property set.


## -struct-fields




### -field guidPropSet

The globally unique identifier (GUID) that identifies the property set.


### -field psProperty

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a> structure that specifies a property either by its property identifier (propid) or by the associated string name (<b>lpwstr</b>).


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/filter/nf-filter-ifilter-init">IFilter::Init</a>
 

 

