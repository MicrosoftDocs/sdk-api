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

# IMFRemoteDesktopPlugin interface


## -description



          Modifies a topology for use in a Terminal Services environment.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRemoteDesktopPlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRemoteDesktopPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRemoteDesktopPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/799ba0b4-b015-4899-9496-d8c23d033b24">UpdateTopology</a>
</td>
<td align="left" width="63%">
Modifies a topology for use in a Terminal Services environment.

</td>
</tr>
</table> 


## -remarks



To use this interface, do the following:

<ol>
<li>
            Call <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> with the <b>SM_REMOTESESSION</b> flag. The function returns <b>TRUE</b> if the calling process is associated with a Terminal Services client session.
          </li>
<li>
            If <b>GetSystemMetrics</b> returns <b>TRUE</b>, call <a href="https://msdn.microsoft.com/c986c80b-b583-47be-91e7-5881db0018c2">MFCreateRemoteDesktopPlugin</a>. This function returns a pointer to the <b>IMFRemoteDesktopPlugin</b> interface.
          </li>
<li>
            Call <a href="https://msdn.microsoft.com/799ba0b4-b015-4899-9496-d8c23d033b24">UpdateTopology</a> with a pointer to the topology.
          </li>
</ol>
The application must call <a href="https://msdn.microsoft.com/799ba0b4-b015-4899-9496-d8c23d033b24">UpdateTopology</a> before calling <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a> on the Media Session.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

