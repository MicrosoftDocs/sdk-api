---
UID: NS:resourceindexer.IndexedResourceQualifier
title: IndexedResourceQualifier
author: windows-sdk-content
description: Represents the context under which a resource is appropriate.
old-location: menurc\indexedresourcequalifier.htm
tech.root: menurc
ms.assetid: A6F253AD-0756-4996-AC6C-5B09C55DE22E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IndexedResourceQualifier, IndexedResourceQualifier structure [Menus and Other Resources], menurc.indexedresourcequalifier, resourceindexer/IndexedResourceQualifier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - resourceindexer.h
api_name:
 - IndexedResourceQualifier
product: Windows
targetos: Windows
req.typenames: IndexedResourceQualifier
req.redist: 
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




<a href="https://msdn.microsoft.com/0E1D8CC6-B662-4068-A6BA-822E79321C33">DestroyIndexedResults</a>



<a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a>
 

 

