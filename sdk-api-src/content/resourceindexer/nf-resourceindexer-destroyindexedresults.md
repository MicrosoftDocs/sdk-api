---
UID: NF:resourceindexer.DestroyIndexedResults
title: DestroyIndexedResults function (resourceindexer.h)
description: Frees the parameters that the IndexFilePath method returned.
helpviewer_keywords: ["DestroyIndexedResults","DestroyIndexedResults function [Menus and Other Resources]","menurc.destroyindexedresults","resourceindexer/DestroyIndexedResults"]
old-location: menurc\destroyindexedresults.htm
tech.root: menurc
ms.assetid: 0E1D8CC6-B662-4068-A6BA-822E79321C33
ms.date: 12/05/2018
ms.keywords: DestroyIndexedResults, DestroyIndexedResults function [Menus and Other Resources], menurc.destroyindexedresults, resourceindexer/DestroyIndexedResults
req.header: resourceindexer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mrmsupport.lib
req.dll: Mrmsupport.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DestroyIndexedResults
 - resourceindexer/DestroyIndexedResults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mrmsupport.dll
api_name:
 - DestroyIndexedResults
---

# DestroyIndexedResults function


## -description

Frees the parameters that the <a href="/windows/desktop/api/resourceindexer/nf-resourceindexer-indexfilepath">IndexFilePath</a> method returned.

## -parameters

### -param resourceUri [in, optional]

A uniform resource indicator (URI) that uses the ms-resource URI scheme and represents the named resource for the candidate, where the authority of the URI or the resource map is empty. For example, ms-resource:///Resources/String1 or ms-resource:///Files/images/logo.png.

### -param qualifierCount [in]

The number of indexed resource qualifiers that the list in the <i>ppQualifiers</i> parameter contains.

### -param qualifiers [in, optional]

A list of indexed resource qualifiers that declare the context under which the resources are appropriate.

## -see-also

<a href="/windows/desktop/api/resourceindexer/nf-resourceindexer-indexfilepath">IndexFilePath</a>



<a href="/windows/desktop/api/resourceindexer/ns-resourceindexer-indexedresourcequalifier">IndexedResourceQualifier</a>