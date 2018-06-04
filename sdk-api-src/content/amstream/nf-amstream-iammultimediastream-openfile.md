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

# IAMMultiMediaStream::OpenFile


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>OpenFile</code> method opens and automatically creates a filter graph for the specified media file. If DirectShow doesn't support the file format, this method does nothing.




## -parameters




### -param pszFileName [in]

Pointer to the name of the file you want to open.


### -param dwFlags [in]

Value that modifies how the filter graph will render the specified file. This value is a combination of one or more of the following flags.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AMMSF_NOCLOCK</td>
<td>Run the stream with no clock.</td>
</tr>
<tr>
<td>AMMSF_NORENDER</td>
<td>Open the file, but do not render any streams. This flag should always be accompanied with the AMMSF_RUN flag.</td>
</tr>
<tr>
<td>AMMSF_RENDERALLSTREAMS</td>
<td>Render all streams, including those that do not have an existing media stream.</td>
</tr>
<tr>
<td>AMMSF_RENDERTOEXISTING</td>
<td>Only render to existing streams.</td>
</tr>
<tr>
<td>AMMSF_RUN</td>
<td>Set the stream into the run state.</td>
</tr>
</table>
 


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
This method tried to access an invalid pointer.

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
 




## -remarks



The AMMSF_RENDERALLSTREAMS flag will create default rendering filters for video and audio if they do not exist. However, these default filters cannot be accessed by the <a href="https://msdn.microsoft.com/dfc38480-7b8d-42ad-937b-dd39384796c9">IStreamSample::GetMediaStream</a> method.




## -see-also




<a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream Interface</a>
 

 

