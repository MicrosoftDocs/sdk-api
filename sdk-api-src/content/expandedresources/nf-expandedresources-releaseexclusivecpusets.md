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

# ReleaseExclusiveCpuSets function


## -description


Opts out of CPU exclusivity, giving the app access to all cores, but at the cost of having to share them with other processes.


## -parameters






## -returns



The result of the operation.




## -remarks



You should call this function when you want to transition to shared mode (for example, if the app is running on a low-end device).

After this function is called, the app will still have access to other Game Mode resources, such as increased GPU prioritization. The app will also still get state transitions via <a href="https://msdn.microsoft.com/E0434DBD-4C1A-4675-94A3-4954BCC67CD5">HasExpandedResources</a>.

As with <a href="https://msdn.microsoft.com/library/windows/desktop/mt186427.aspx">SetProcessDefaultCpuSets</a>, <b>ReleaseExclusiveCpuSets</b> applies to the whole process.

This is a Win32 API that's only supported in UWP desktop and Xbox apps. It also requires the <b>expandedResources</b> restricted capability, which you can select by opening <b>Package.appxmanifest</b> in Visual Studio and navigating to the <b>Capabilities</b> tab. Alternatively, you can edit the file's code directly:

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>
&lt;Package
xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
IgnorableNamespaces=" rescap"&gt;
	...
	&lt;Capabilities&gt;
		&lt;rescap:Capability Name="expandedResources" /&gt;
	&lt;/Capabilities&gt;
	...
&lt;/Package&gt;</pre>
</td>
</tr>
</table></span></div>
This capability is granted on a per-title basis; contact your account manager for more information. You can publish a UWP app with this capability to the Store if it targets desktop, but if it targets Xbox it will be rejected in certification.

The app must be in the foreground and have focus before exclusive resources are granted.



