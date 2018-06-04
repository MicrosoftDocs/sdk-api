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

# IWMIndexer::StartIndexing


## -description



The <b>StartIndexing</b> method initiates indexing. If you configure the indexer using the <a href="https://msdn.microsoft.com/b4ab9ad8-5fc7-43ce-ba2f-f32135a44a86">IWMIndexer2::Configure</a> method, <b>StartIndexing</b> creates an index based upon your configuration. When you use <b>StartIndexing</b> without first calling <b>Configure</b>, the indexer creates a default temporal index.




## -parameters




### -param pwszURL [in]

Pointer to a wide-character <b>null</b>-terminated string containing the URL or file name.


### -param pCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> interface.


### -param pvContext [in]

Generic pointer, for use by the application.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter <i>pwszURL</i> or <i>pCallback</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The method cannot start indexing in the current state.

</td>
</tr>
</table>
 




## -remarks



<b>StartIndexing</b> is an asynchronous call; it returns almost immediately and the application must wait for appropriate <b>OnStatus</b> calls to be sent to the callback function.

If you call <b>StartIndexing</b> for a file that is already indexed, the old index is discarded.

When the indexer successfully indexes a file, it will set some of the reserved attribute values as described in the following table.

<table>
<tr>
<th>
              Index type
            </th>
<th>
              Attributes set
            </th>
</tr>
<tr>
<td>WMT_IT_PRESENTATION_TIME</td>
<td>
g_wszWMSeekable

g_wszWMStridable, if a video stream is present.

</td>
</tr>
<tr>
<td>WMT_IT_FRAME_NUMBERS</td>
<td>
g_wszWMNumberOfFrames

g_wszWMSeekable

g_wszWMStridable

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer Interface</a>



<a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a>
 

 

