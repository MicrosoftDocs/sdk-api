---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _avisuperindex structure


## -description


Contains an AVI 2.0 super index (index of indexes).


## -struct-fields




### -field fcc

A <b>FOURCC</b> code. The value must be 'indx'.


### -field cb

The size of the structure, not including the initial 8 bytes.


### -field wLongsPerEntry

The size of each index entry, in 4-byte units. The value must be 4.


### -field bIndexSubType

The index subtype. The value must be zero or <b>AVI_INDEX_SUB_2FIELD</b>.


### -field bIndexType

The index type. The value must be <b>AVI_INDEX_OF_INDEXES</b>.


### -field nEntriesInUse

The number of valid entries in the <b>adwIndex</b> array.


### -field dwChunkId

A <b>FOURCC</b> that identifies the object that is indexed.


### -field dwReserved

Reserved. Set the array elements to zero.


### -field _avisuperindex_entry

 


### -field _avisuperindex_entry.qwOffset

 


### -field _avisuperindex_entry.dwSize

 


### -field _avisuperindex_entry.dwDuration

 


### -field aIndex

An array of structures that contain the following members. The number of elements in the array is calculated from the value of <b>cb</b>.



#### qwOffset

The offset, in bytes, from the start of the file to the sub-index that this entry points to.



#### dwSize

The size of the sub-index, in bytes.



#### dwDuration


              
            The duration of the file that is covered by the sub-index, in stream ticks.


## -remarks



For more information, see the <i>OpenDML AVI File Format Extensions</i>, published by the OpenDML AVI M-JPEG File Format Subcommittee. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/2d8cf5be-1252-4b58-89b1-f5c53ea17d0e">AVI RIFF File Reference</a>



<a href="https://msdn.microsoft.com/d27b2b14-55a1-4992-ad85-75244369accc">AVIMETAINDEX</a>



<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

