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

# IMFSourceReaderCallback::OnReadSample


## -description


Called when the <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> method completes.


## -parameters




### -param hrStatus [in]

The status code. If an error occurred while processing the next sample, this parameter contains the error code. 


### -param dwStreamIndex [in]

The zero-based index of the stream that delivered the sample.


### -param dwStreamFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/8981a682-3c0b-458b-910a-d1462ed73e64">MF_SOURCE_READER_FLAG</a> enumeration.


### -param llTimestamp [in]

The time stamp of the sample, or the time of the stream event indicated in <i>dwStreamFlags</i>. The time is given in 100-nanosecond units.



### -param pSample [in]

A pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of a media sample. This parameter might be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Currently, the source reader ignores the return value.




## -remarks



The <i>pSample</i> parameter might be <b>NULL</b>. For example, when the source reader reaches the end of a stream, <i>dwStreamFlags</i> contains the <b>MF_SOURCE_READERF_ENDOFSTREAM</b> flag, and <i>pSample</i> is <b>NULL</b>.



If there is a gap in the stream, <i>dwStreamFlags</i> contains the <b>MF_SOURCE_READERF_STREAMTICK</b> flag, <i>pSample</i> is <b>NULL</b>, and <i>llTimestamp</i> indicates the time when the gap occurred. 



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/fff8b6e6-5d56-4301-b3ce-f3ff49398593">IMFSourceReaderCallback</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

