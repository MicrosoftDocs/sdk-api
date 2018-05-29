---
UID: NF:mediaobj.IMediaObject.GetOutputStreamInfo
title: IMediaObject::GetOutputStreamInfo
author: windows-sdk-content
description: The GetOutputStreamInfo method retrieves information about an output stream; for example, whether the stream is discardable, and whether it uses a fixed sample size. This information never changes.
old-location: dshow\imediaobject_getoutputstreaminfo.htm
old-project: DirectShow
ms.assetid: a21e9943-4aaf-4f0e-a92a-5fcd551fe7e1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetOutputStreamInfo, GetOutputStreamInfo method [DirectShow], GetOutputStreamInfo method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetOutputStreamInfo method, IMediaObject.GetOutputStreamInfo, IMediaObject::GetOutputStreamInfo, IMediaObjectGetOutputStreamInfo, dshow.imediaobject_getoutputstreaminfo, mediaobj/IMediaObject::GetOutputStreamInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dmoguids.lib
-	Dmoguids.dll
api_name:
-	IMediaObject.GetOutputStreamInfo
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::GetOutputStreamInfo


## -description



The <code>GetOutputStreamInfo</code> method retrieves information about an output stream; for example, whether the stream is discardable, and whether it uses a fixed sample size. This information never changes.




## -parameters




### -param dwOutputStreamIndex

Zero-based index of an output stream on the DMO.


### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of zero or more <a href="https://msdn.microsoft.com/570dd009-0101-4a01-b064-4f4404fb453f">DMO_OUTPUT_STREAM_INFO_FLAGS</a> flags.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>
 

 

