---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataWriter.WriteNextItem
title: ISpatialAudioMetadataWriter::WriteNextItem
author: windows-driver-content
description: Starts a new metadata item at the specified offset.
old-location: coreaudio\ispatialaudiometadatawriter_writenextitem.htm
old-project: CoreAudio
ms.assetid: 9D61BFC0-BAD7-46D3-B0E9-4848E37785E9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISpatialAudioMetadataWriter interface [Core Audio],WriteNextItem method, ISpatialAudioMetadataWriter.WriteNextItem, ISpatialAudioMetadataWriter::WriteNextItem, WriteNextItem, WriteNextItem method [Core Audio], WriteNextItem method [Core Audio],ISpatialAudioMetadataWriter interface, coreaudio.ispatialaudiometadatawriter_writenextitem, spatialaudiometadata/ISpatialAudioMetadataWriter::WriteNextItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SpatialAudioMetadata.h
api_name:
-	ISpatialAudioMetadataWriter.WriteNextItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioMetadataWriter::WriteNextItem


## -description


Starts a new metadata item at the specified offset.


## -parameters




### -param frameOffset [in]

The frame offset of the item within the range specified with the <i>frameCount</i> parameter to <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a>.


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
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for writing with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The number of items written in the writing session is greater than the value supplied in the <b>MaxMetadataItemCount</b> field in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParam</a> passed into <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a>. 

The <i>frameCount</i> value is greater than the value of the <i>frameCount</i> parameter to <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a> and the overflow mode was set to  <b>SpatialAudioMetadataWriterOverflow_Fail</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>frameOffset</i> is not greater than the value provided  in the previous call to <a href="https://msdn.microsoft.com/9D61BFC0-BAD7-46D3-B0E9-4848E37785E9">WriteNextItem</a> within the same writing session.

</td>
</tr>
</table>
 




## -remarks



Before calling <b>WriteNextItem</b>, you must open the <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> for writing by calling <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> after the object is created and after <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a> has been called. During a writing session demarcated by calls to <b>Open</b> and <b>Close</b>, the value of the <i>frameOffset</i> parameter must be greater than the value in the preceding call.  

Within a single writing session, you must not use <b>WriteNextItem</b> to write more items than the value supplied in the <b>MaxMetadataItemCount</b> field in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParam</a> passed into <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a> or an SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE error will occur. 

If the overflow mode is set to <b>SpatialAudioMetadataWriterOverflow_Fail</b>, the value of the <i>frameOffset</i> parameter must be less than he value of the <i>frameCount</i> parameter to <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a> or an SPTLAUD_MD_CLNT_E_FRAMEOFFSET_OUT_OF_RANGE error will occur.

After calling <b>WriteNextItem</b>, call <a href="https://msdn.microsoft.com/A614AEC6-7CA3-4624-BAFE-46618BCB64FA">WriteNextItemCommand</a> to write metadata commands and value data for the item.




## -see-also




<a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>
 

 

