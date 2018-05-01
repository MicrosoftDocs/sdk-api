---
UID: NS:filter.tagFULLPROPSPEC
title: tagFULLPROPSPEC
author: windows-driver-content
description: Specifies a property set and a property within the property set.
old-location: indexsrv\fullpropspec.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_599f.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: FULLPROPSPEC, FULLPROPSPEC structure [Indexing Service], _idxs_FULLPROPSPEC, filter/FULLPROPSPEC, indexsrv.fullpropspec, tagFULLPROPSPEC
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FULLPROPSPEC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Filter.h
api_name:
-	FULLPROPSPEC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# tagFULLPROPSPEC structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies a property set and a property within the property set.


## -struct-fields




### -field guidPropSet

The globally unique identifier (GUID) that identifies the property set.


### -field psProperty

A pointer to the <a href="_stg_propspec">PROPSPEC</a> structure that specifies a property either by its property identifier (propid) or by the associated string name (<b>lpwstr</b>).


## -see-also




<a href="https://msdn.microsoft.com/5cb9b675-258e-46b0-905f-15a086f84f74">IFilter::Init</a>
 

 

