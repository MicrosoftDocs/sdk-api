---
UID: NF:mmstream.IMultiMediaStream.GetInformation
title: IMultiMediaStream::GetInformation
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetInformation method retrieves the capabilities of the multimedia stream object.
old-location: dshow\imultimediastream_getinformation.htm
old-project: DirectShow
ms.assetid: 27be6104-9ca4-48d7-aeda-5b633460e252
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetInformation, GetInformation method [DirectShow], GetInformation method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetInformation method, IMultiMediaStream.GetInformation, IMultiMediaStream::GetInformation, IMultiMediaStreamGetInformation, dshow.imultimediastream_getinformation, mmstream/IMultiMediaStream::GetInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmstream.h
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
req.typenames: STREAM_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMultiMediaStream.GetInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMultiMediaStream::GetInformation


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetInformation</code> method retrieves the capabilities of the multimedia stream object.




## -parameters




### -param pdwFlags [out]

Pointer to a variable that receives a bitwise combination of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MMSSF_ASYNCHRONOUS</td>
<td>The object supports asynchronous sample updates. This flag is always returned.</td>
</tr>
<tr>
<td>MMSSF_HASCLOCK</td>
<td>The object has a clock.</td>
</tr>
<tr>
<td>MMSSF_SUPPORTSEEK</td>
<td>The object supports seeking.</td>
</tr>
</table>
 

This parameter can be <b>NULL</b>.


### -param pStreamType [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/07ab5ded-28b8-4cac-b4da-76f07ad351ef">STREAM_TYPE</a> enumeration. This value indicates whether the multimedia stream is read-only, write-only, or read/write. This parameter can be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

