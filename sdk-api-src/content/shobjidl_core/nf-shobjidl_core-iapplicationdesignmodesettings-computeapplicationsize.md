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

# IApplicationDesignModeSettings::ComputeApplicationSize


## -description


Gets the size of the Windows Store app, based on the current set of spoofed settings.

You must call <a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method.

In addition, each of these methods must be called before calling <b>ComputeApplicationSize</b>, or the call will fail.

                <ul>
<li>
<a href="https://msdn.microsoft.com/37e1845c-a58a-4da3-b259-bbf5bbf5ff6d">SetApplicationViewState</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fc301573-6550-4e21-b82b-7800bbf34ea6">SetNativeDisplaySize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/55b80010-a71e-44c2-8105-e9f5b9a833f5">SetScaleFactor</a>
</li>
</ul>



## -parameters




### -param applicationSizePixels [out]

When this method returns successfully, receives a pointer to the size that the Windows Store app should occupy, based on the current set of spoofed settings.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> has not been called to set a proxy core window.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>
 

 

