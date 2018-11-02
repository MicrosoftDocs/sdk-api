---
UID: NS:wmcontainer._ASF_INDEX_IDENTIFIER
title: "_ASF_INDEX_IDENTIFIER"
author: windows-sdk-content
description: Specifies an index for the ASF indexer object.
old-location: mf\asf_index_identifier.htm
tech.root: medfound
ms.assetid: 8103a62e-6d1a-4dcd-af91-cedb30523004
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 8103a62e-6d1a-4dcd-af91-cedb30523004, ASF_INDEX_IDENTIFIER, ASF_INDEX_IDENTIFIER structure [Media Foundation], _ASF_INDEX_IDENTIFIER, mf.asf_index_identifier, wmcontainer/ASF_INDEX_IDENTIFIER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - wmcontainer.h
api_name:
 - ASF_INDEX_IDENTIFIER
product: Windows
targetos: Windows
req.typenames: ASF_INDEX_IDENTIFIER
req.redist: 
---

# _ASF_INDEX_IDENTIFIER structure


## -description


Specifies an index for the ASF indexer object.
        


## -struct-fields




### -field guidIndexType

The type of index. Currently this value must be GUID_NULL, which specifies time-based indexing.
          


### -field wStreamNumber

The stream number to which this structure applies.
          


## -remarks



The index object of an ASF file can contain a number of distinct indexes. Each index is identified by the type of index and the stream number. No ASF index object can contain more than one index for a particular combination of stream number and index type.




## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/dc38a060-36e4-458e-829e-2770387fc484">IMFASFIndexer::GetIndexStatus</a>



<a href="https://msdn.microsoft.com/bad10893-07af-4b46-bab1-2878553813b5">IMFASFIndexer::SetIndexStatus</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

