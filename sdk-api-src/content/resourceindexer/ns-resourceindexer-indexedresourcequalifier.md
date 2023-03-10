---
UID: NS:resourceindexer.IndexedResourceQualifier
title: IndexedResourceQualifier (resourceindexer.h)
description: Represents the context under which a resource is appropriate.
helpviewer_keywords: ["IndexedResourceQualifier","IndexedResourceQualifier structure [Menus and Other Resources]","menurc.indexedresourcequalifier","resourceindexer/IndexedResourceQualifier"]
old-location: menurc\indexedresourcequalifier.htm
tech.root: menurc
ms.assetid: A6F253AD-0756-4996-AC6C-5B09C55DE22E
ms.date: 12/05/2018
ms.keywords: IndexedResourceQualifier, IndexedResourceQualifier structure [Menus and Other Resources], menurc.indexedresourcequalifier, resourceindexer/IndexedResourceQualifier
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IndexedResourceQualifier
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IndexedResourceQualifier
 - resourceindexer/IndexedResourceQualifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - resourceindexer.h
api_name:
 - IndexedResourceQualifier
---

# IndexedResourceQualifier structure


## -description

Represents the context under which a resource is appropriate.

## -struct-fields

### -field name

The name of the qualifier, such as "language", "contrast", or "scale".

### -field value

The value of the qualifier. You should preserve the case of the qualifier value from the first instance of the qualifier discovered during indexing.



The following values are examples of the qualifier values:

<ul>
<li>"100", "140", or "180" for scale.</li>
<li>"fr-FR" for language.</li>
<li>"high" for contrast.
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/resourceindexer/nf-resourceindexer-destroyindexedresults">DestroyIndexedResults</a>



<a href="/windows/desktop/api/resourceindexer/nf-resourceindexer-indexfilepath">IndexFilePath</a>

