---
UID: NN:mfidl.IMFRemoteDesktopPlugin
title: IMFRemoteDesktopPlugin
author: windows-sdk-content
description: Modifies a topology for use in a Terminal Services environment.
old-location: mf\imfremotedesktopplugin.htm
old-project: medfound
ms.assetid: 75bb9bf8-12a7-430f-9943-18623aff9903
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 75bb9bf8-12a7-430f-9943-18623aff9903, IMFRemoteDesktopPlugin, IMFRemoteDesktopPlugin interface [Media Foundation], IMFRemoteDesktopPlugin interface [Media Foundation],described, mf.imfremotedesktopplugin, mfidl/IMFRemoteDesktopPlugin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFRemoteDesktopPlugin
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

