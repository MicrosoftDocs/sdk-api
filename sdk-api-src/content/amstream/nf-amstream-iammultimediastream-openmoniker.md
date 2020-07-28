---
UID: NF:amstream.IAMMultiMediaStream.OpenMoniker
title: IAMMultiMediaStream::OpenMoniker (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The OpenMoniker method opens a file or device moniker; you can read media data from this moniker if DirectShow supports the moniker.
helpviewer_keywords: ["IAMMultiMediaStream interface [DirectShow]","OpenMoniker method","IAMMultiMediaStream.OpenMoniker","IAMMultiMediaStream::OpenMoniker","IAMMultiMediaStreamOpenMoniker","OpenMoniker","OpenMoniker method [DirectShow]","OpenMoniker method [DirectShow]","IAMMultiMediaStream interface","amstream/IAMMultiMediaStream::OpenMoniker","dshow.iammultimediastream_openmoniker"]
old-location: dshow\iammultimediastream_openmoniker.htm
tech.root: dshow
ms.assetid: ccfed197-6637-4283-9996-56049da49b84
ms.date: 12/05/2018
ms.keywords: IAMMultiMediaStream interface [DirectShow],OpenMoniker method, IAMMultiMediaStream.OpenMoniker, IAMMultiMediaStream::OpenMoniker, IAMMultiMediaStreamOpenMoniker, OpenMoniker, OpenMoniker method [DirectShow], OpenMoniker method [DirectShow],IAMMultiMediaStream interface, amstream/IAMMultiMediaStream::OpenMoniker, dshow.iammultimediastream_openmoniker
f1_keywords:
- amstream/IAMMultiMediaStream.OpenMoniker
dev_langs:
- c++
req.header: amstream.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- amstream.h
api_name:
- IAMMultiMediaStream.OpenMoniker
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMultiMediaStream::OpenMoniker


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>OpenMoniker</code> method opens a file or device moniker; you can read media data from this moniker if DirectShow supports the moniker.




## -parameters




### -param pCtx [in]

Pointer to the bind context associated with the moniker.


### -param pMoniker [in]

Pointer to an <b>IMoniker</b> interface that specifies the moniker you want to open.


### -param dwFlags [in]

Value that modifies how the filter graph will render the specified file. This value is a combination of one or more of the following flags.

<table>
<tr>
<th>Value
                </th>
<th>Description
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



Returns S_OK if successful or E_INVALIDARG if the <i>dwFlags</i> parameter is invalid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream Interface</a>
 

 

