---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataReader.ReadNextItem
title: ISpatialAudioMetadataReader::ReadNextItem
author: windows-sdk-content
description: Gets the number of commands and the sample offset for the metadata item being read.
old-location: coreaudio\ispatialaudiometadatareader_readnextitem.htm
old-project: CoreAudio
ms.assetid: AC1D5FD6-EFF1-410F-95C7-B13EACBED5D1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISpatialAudioMetadataReader interface [Core Audio],ReadNextItem method, ISpatialAudioMetadataReader.ReadNextItem, ISpatialAudioMetadataReader::ReadNextItem, ReadNextItem, ReadNextItem method [Core Audio], ReadNextItem method [Core Audio],ISpatialAudioMetadataReader interface, coreaudio.ispatialaudiometadatareader_readnextitem, spatialaudiometadata/ISpatialAudioMetadataReader::ReadNextItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudiometadata.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SpatialAudioMetadata.h
api_name:
-	ISpatialAudioMetadataReader.ReadNextItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataReader::ReadNextItem


## -description


Gets the number of commands and the sample offset for the metadata item being read.


## -parameters




### -param commandCount [out]

Receives the number of command/value pairs in the metadata item being read.


### -param frameOffset [out]

Gets the frame offset associated with the metadata item being read.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for reading with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more metadata items in the frame range specified in the call to <a href="https://msdn.microsoft.com/E9958586-0B1E-4864-AE0F-A9805114A797">ReadItemCountInFrames</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

</td>
</tr>
</table>
 




## -remarks



Before calling <b>ReadNextItem</b>, you must open the <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a> for reading by calling <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> after the object is created and after <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> has been called. You must also call <a href="https://msdn.microsoft.com/E9958586-0B1E-4864-AE0F-A9805114A797">ReadItemCountInFrames</a> before calling <b>ReadNextItem</b>.

The <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a> keeps an internal pointer to the current position within the total range of frames contained by the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> with which the reader is associated. Each call to this method causes the pointer to be advanced by the number of frames specified in the <i>readFrameCount</i> parameter.

The process for reading commands and the associated values is recursive. After each call to <b>ReadItemCountInFrames</b>, call <b>ReadNextItem</b> to get the number of commands in the next item. After every call to <b>ReadNextItem</b>, call <a href="https://msdn.microsoft.com/9B58546A-FBE3-47CD-8E5F-63D0C5608F00">ReadNextItemCommand</a> to read each command for the  item. Repeat this process until the entire frame range of the <b>ISpatialAudioMetadataItems</b> has been read.




## -see-also




<a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>
 

 

