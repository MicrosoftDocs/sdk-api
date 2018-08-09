---
UID: NS:filter.tagFULLPROPSPEC
title: tagFULLPROPSPEC
author: windows-sdk-content
description: Specifies a property set and a property within the property set.
old-location: indexsrv\fullpropspec.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_599f.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FULLPROPSPEC, FULLPROPSPEC structure [Indexing Service], _idxs_FULLPROPSPEC, filter/FULLPROPSPEC, indexsrv.fullpropspec, tagFULLPROPSPEC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: FULLPROPSPEC
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
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# tagFULLPROPSPEC structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies a property set and a property within the property set.


## -struct-fields




### -field guidPropSet

The globally unique identifier (GUID) that identifies the property set.


### -field psProperty

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa380070(v=VS.85).aspx">PROPSPEC</a> structure that specifies a property either by its property identifier (propid) or by the associated string name (<b>lpwstr</b>).


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690965(v=VS.85).aspx">IFilter::Init</a>
 

 

