---
UID: NS:wmcontainer._ASF_INDEX_DESCRIPTOR
title: "_ASF_INDEX_DESCRIPTOR"
author: windows-driver-content
description: Describes the indexing configuration for a stream and type of index.
old-location: mf\asf_index_descriptor.htm
old-project: medfound
ms.assetid: 2a540aef-068d-4465-b0ed-64aed828af01
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 2a540aef-068d-4465-b0ed-64aed828af01, ASF_INDEX_DESCRIPTOR, ASF_INDEX_DESCRIPTOR structure [Media Foundation], _ASF_INDEX_DESCRIPTOR, mf.asf_index_descriptor, wmcontainer/ASF_INDEX_DESCRIPTOR
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: ASF_INDEX_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wmcontainer.h
api_name:
-	ASF_INDEX_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ASF_INDEX_DESCRIPTOR structure


## -description



Describes the indexing configuration for a stream and type of index.




## -struct-fields




### -field Identifier


<a href="https://msdn.microsoft.com/8103a62e-6d1a-4dcd-af91-cedb30523004">ASF_INDEX_IDENTIFIER</a> structure that identifies the stream number and the type of index.


### -field cPerEntryBytes

Number of bytes used for each index entry. If the value is MFASFINDEXER_PER_ENTRY_BYTES_DYNAMIC, the index entries have variable size.


### -field szDescription

Optional text description of the index.


### -field dwInterval

Indexing interval. The units of this value depend on the index type. A value of MFASFINDEXER_NO_FIXED_INTERVAL indicates that there is no fixed indexing interval.


## -see-also




<a href="https://msdn.microsoft.com/3f95b0ac-d70f-4bc2-8524-c7de1df34afa">ASF Index Object</a>



<a href="https://msdn.microsoft.com/dc38a060-36e4-458e-829e-2770387fc484">IMFASFIndexer::GetIndexStatus</a>



<a href="https://msdn.microsoft.com/bad10893-07af-4b46-bab1-2878553813b5">IMFASFIndexer::SetIndexStatus</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

