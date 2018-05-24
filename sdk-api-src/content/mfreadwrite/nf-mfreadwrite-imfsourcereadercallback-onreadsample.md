---
UID: NF:mfreadwrite.IMFSourceReaderCallback.OnReadSample
title: IMFSourceReaderCallback::OnReadSample
author: windows-driver-content
description: Called when the IMFSourceReader::ReadSample method completes.
old-location: mf\imfsourcereadercallback_onreadsample.htm
old-project: medfound
ms.assetid: 1f334b49-d297-478d-a037-2fc53a75ed52
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFSourceReaderCallback interface [Media Foundation],OnReadSample method, IMFSourceReaderCallback.OnReadSample, IMFSourceReaderCallback::OnReadSample, OnReadSample, OnReadSample method [Media Foundation], OnReadSample method [Media Foundation],IMFSourceReaderCallback interface, mf.imfsourcereadercallback_onreadsample, mfreadwrite/IMFSourceReaderCallback::OnReadSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSourceReaderCallback.OnReadSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

