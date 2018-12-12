---
UID: NN:segment.IMSVidStreamBufferSink
title: IMSVidStreamBufferSink
author: windows-sdk-content
description: The IMSVidStreamBufferSink interface represents the Stream Buffer Sink filter within the Video Control.
old-location: mstv\imsvidstreambuffersink.htm
tech.root: mstv
ms.assetid: 80f6cd3a-8cb8-4bda-9b66-33e7d214015a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidStreamBufferSink, IMSVidStreamBufferSink interface [Microsoft TV Technologies], IMSVidStreamBufferSink interface [Microsoft TV Technologies],described, IMSVidStreamBufferSinkInterface, mstv.imsvidstreambuffersink, segment/IMSVidStreamBufferSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSink interface


## -description



The <b>IMSVidStreamBufferSink</b> interface represents the Stream Buffer Sink filter within the Video Control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidStreamBufferSink</b> interface inherits from <a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>. <b>IMSVidStreamBufferSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidStreamBufferSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694655(v=VS.85).aspx">get_ContentRecorder</a>
</td>
<td align="left" width="63%">
Creates a new content recording object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694656(v=VS.85).aspx">get_ReferenceRecorder</a>
</td>
<td align="left" width="63%">
Creates a new reference recording object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694657(v=VS.85).aspx">get_SBESink</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the Stream Buffer Sink filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694658(v=VS.85).aspx">get_SinkName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the stub file that points to the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694659(v=VS.85).aspx">NameSetLock</a>
</td>
<td align="left" width="63%">
Locks the stream buffer profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694660(v=VS.85).aspx">put_SinkName</a>
</td>
<td align="left" width="63%">
Sets the name of the stub file that points to the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidStreamBufferSink)</code>.




## -see-also




<a href="https://msdn.microsoft.com/c2e5ebac-cb10-4567-83f7-f8f4e3b4f009">IMSVidOutputDevice</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

