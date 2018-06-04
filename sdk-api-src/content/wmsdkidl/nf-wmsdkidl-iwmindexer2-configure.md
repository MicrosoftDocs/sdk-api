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

# IWMIndexer2::Configure


## -description



The <b>Configure</b> method changes the internal settings of the indexer object. You can use <b>Configure</b> to activate frame-based indexing or SMPTE time code indexing. <b>Configure</b> does not create an index, it just configures the indexer object. After you have changed the desired settings, you must call <a href="https://msdn.microsoft.com/67dfb0df-4883-49e1-a085-0b78db3967d0">IWMIndexer::StartIndexing</a> to create the index.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which an index is to be made. If you pass 0, all streams will be indexed.


### -param nIndexerType [in]

A variable containing one member of the <a href="https://msdn.microsoft.com/1b80511c-175f-4d05-8ce6-d048a9e77223">WMT_INDEXER_TYPE</a> enumeration type.


### -param pvInterval [in]

This void pointer must point to a <b>DWORD</b> containing the desired indexing interval. Intervals for temporal indexing are in milliseconds. Frame-based index intervals are specified in frames.

If you pass <b>NULL</b>, <b>Configure</b> will use the default value. For temporal indexes, the default value is 3000 milliseconds, for frame-based indexes it is 10 frames.


### -param pvIndexType [in]

This void pointer must point to a <b>WORD</b> value containing one member of the <a href="https://msdn.microsoft.com/250f12ba-2334-41e4-9258-0da79dd4cb3d">WMT_INDEX_TYPE</a> enumeration type. If you pass <b>NULL</b>, <b>Configure</b> will use the default value.

The default value is WMT_IT_NEAREST_CLEAN_POINT. Using another index type degrades seeking performance.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to add the stream number to its internal list.

</td>
</tr>
</table>
 




## -remarks



You can call <b>Configure</b> as many times as needed to configure multiple streams in a file. You must make all desired calls to <b>Configure</b> before you start indexing. If you configure and index a file that already has an index, the existing index will be deleted.

If you configure the indexer to build a frame-based index, it will also create a temporal index. This is required for synchronizing audio and video.




## -see-also




<a href="https://msdn.microsoft.com/ce900a2b-765b-46bb-87f4-bf9fe57d1cdb">IWMIndexer2 Interface</a>
 

 

