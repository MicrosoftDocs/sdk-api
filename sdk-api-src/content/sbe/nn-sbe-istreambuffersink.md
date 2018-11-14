---
UID: NN:sbe.IStreamBufferSink
title: IStreamBufferSink
author: windows-sdk-content
description: The IStreamBufferSink interface is exposed by the Stream Buffer Sink filter. Use this interface to lock the filter before capture and to create new recordings.
old-location: mstv\istreambuffersink.htm
tech.root: MSTV
ms.assetid: 4ae5a9e9-da51-4034-9a2c-22b57374deac
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IStreamBufferSink, IStreamBufferSink interface [Microsoft TV Technologies], IStreamBufferSink interface [Microsoft TV Technologies],described, IStreamBufferSinkInterface, mstv.istreambuffersink, sbe/IStreamBufferSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Sbe.h
api_name:
 - IStreamBufferSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferSink interface


## -description



The <b>IStreamBufferSink</b> interface is exposed by the <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter. Use this interface to lock the filter before capture and to create new recordings.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9f3b7e1-4f54-4802-af24-4b791ee646fc">CreateRecorder</a>
</td>
<td align="left" width="63%">
Creates a <b>Recording</b> object for permanent file storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/941c1702-2ef2-4afe-933c-78ed9ee8690b">IsProfileLocked</a>
</td>
<td align="left" width="63%">
Indicates whether the profile has been locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">LockProfile</a>
</td>
<td align="left" width="63%">
Locks a graph profile, preventing input streams from changing, and optionally specifies the buffer file's name and location.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSink)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>



<a href="https://msdn.microsoft.com/aa19d268-fbeb-4dc4-a8f5-8bc31a85367f">Using the Stream Buffer Engine</a>
 

 

