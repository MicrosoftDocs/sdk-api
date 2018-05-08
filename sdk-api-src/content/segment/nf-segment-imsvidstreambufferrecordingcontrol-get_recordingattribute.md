---
UID: NF:segment.IMSVidStreamBufferRecordingControl.get_RecordingAttribute
title: IMSVidStreamBufferRecordingControl::get_RecordingAttribute
author: windows-driver-content
description: The get_RecordingAttribute method retrieves the stream buffer Recording object that is controlled by this interface.
old-location: mstv\imsvidstreambufferrecordingcontrol_get_recordingattribute.htm
old-project: mstv
ms.assetid: 259d0ca0-0566-443c-aa73-a28c304b9d1d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidStreamBufferRecordingControl interface [Microsoft TV Technologies],get_RecordingAttribute method, IMSVidStreamBufferRecordingControl.get_RecordingAttribute, IMSVidStreamBufferRecordingControl::get_RecordingAttribute, IMSVidStreamBufferRecordingControlget_RecordingAttribute, get_RecordingAttribute, get_RecordingAttribute method [Microsoft TV Technologies], get_RecordingAttribute method [Microsoft TV Technologies],IMSVidStreamBufferRecordingControl interface, mstv.imsvidstreambufferrecordingcontrol_get_recordingattribute, segment/IMSVidStreamBufferRecordingControl::get_RecordingAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidStreamBufferRecordingControl.get_RecordingAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidStreamBufferRecordingControl::get_RecordingAttribute


## -description


The <b>get_RecordingAttribute</b> method retrieves the stream buffer <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> object that is controlled by this interface.


## -parameters




### -param pRecordingAttribute [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/717a3b99-d998-4e64-aab6-6b06e18991da">Recording</a> object's <b>IUnknown</b> interface.


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



The caller must release the returned <b>IUnknown</b> pointer.




## -see-also




<a href="https://msdn.microsoft.com/a61414dc-a9a0-4c65-8f5a-eaabc79783e3">IMSVidStreamBufferRecordingControl Interface</a>
 

 

