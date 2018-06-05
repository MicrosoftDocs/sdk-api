---
UID: NF:segment.IMSVidStreamBufferSource.get_RecordingAttribute
title: IMSVidStreamBufferSource::get_RecordingAttribute
author: windows-sdk-content
description: The get_RecordingAttribute method retrieves the Stream Buffer Source filter that this object manages.
old-location: mstv\imsvidstreambuffersource_get_recordingattribute.htm
old-project: mstv
ms.assetid: 9e7020c8-778d-4a24-ae29-3e66d4ac165a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],get_RecordingAttribute method, IMSVidStreamBufferSource.get_RecordingAttribute, IMSVidStreamBufferSource::get_RecordingAttribute, IMSVidStreamBufferSourceget_RecordingAttribute, get_RecordingAttribute, get_RecordingAttribute method [Microsoft TV Technologies], get_RecordingAttribute method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_get_recordingattribute, segment/IMSVidStreamBufferSource::get_RecordingAttribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferSource.get_RecordingAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidStreamBufferSource::get_RecordingAttribute


## -description


The <b>get_RecordingAttribute</b> method retrieves the <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter that this object manages.


## -parameters




### -param pRecordingAttribute [out]

Receives a pointer to the filter's <b>IUnknown</b> interface.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

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
</table>
 




## -remarks



The caller must release the returned <b>IUnknown</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource Interface</a>
 

 

