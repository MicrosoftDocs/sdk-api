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



Returns S_OK if successful or E_INVALIDARG if the <i>dwFlags</i> parameter is invalid.




## -see-also




<a href="https://msdn.microsoft.com/2f604156-68ef-4770-9929-6dbfd46c4d6d">IAMMultiMediaStream Interface</a>
 

 

