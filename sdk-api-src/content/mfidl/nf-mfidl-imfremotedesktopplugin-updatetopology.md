---
UID: NF:mfidl.IMFRemoteDesktopPlugin.UpdateTopology
title: IMFRemoteDesktopPlugin::UpdateTopology method
author: windows-driver-content
description: Modifies a topology for use in a Terminal Services environment.
old-location: mf\imfremotedesktopplugin_updatetopology.htm
old-project: medfound
ms.assetid: 799ba0b4-b015-4899-9496-d8c23d033b24
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 799ba0b4-b015-4899-9496-d8c23d033b24, IMFRemoteDesktopPlugin, IMFRemoteDesktopPlugin interface [Media Foundation], UpdateTopology method, IMFRemoteDesktopPlugin::UpdateTopology, UpdateTopology method [Media Foundation], UpdateTopology method [Media Foundation], IMFRemoteDesktopPlugin interface, UpdateTopology,IMFRemoteDesktopPlugin.UpdateTopology, mf.imfremotedesktopplugin_updatetopology, mfidl/IMFRemoteDesktopPlugin::UpdateTopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFRemoteDesktopPlugin.UpdateTopology
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRemoteDesktopPlugin::UpdateTopology method


## -description



Modifies a topology for use in a Terminal Services environment.




## -parameters




### -param pTopology [in, out]

Pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the topology.


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
</table>
 




## -remarks



If the application is running in a Terminal Services client session, call this method before calling <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a> on the Media Session.




## -see-also




<a href="https://msdn.microsoft.com/75bb9bf8-12a7-430f-9943-18623aff9903">IMFRemoteDesktopPlugin</a>
 

 

