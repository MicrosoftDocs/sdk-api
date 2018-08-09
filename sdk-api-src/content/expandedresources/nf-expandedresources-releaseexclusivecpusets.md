---
UID: NF:expandedresources.ReleaseExclusiveCpuSets
title: ReleaseExclusiveCpuSets function
author: windows-sdk-content
description: Opts out of CPU exclusivity, giving the app access to all cores, but at the cost of having to share them with other processes.
old-location: gamemode\releaseexclusivecpusets.htm
old-project: gamemode
ms.assetid: C30D28CF-1A35-4849-AEC4-74F971C5F9DF
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ReleaseExclusiveCpuSets, ReleaseExclusiveCpuSets function, expandedresources/ReleaseExclusiveCpuSets, gamemode.releaseexclusivecpusets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: expandedresources.h
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gamemode.dll
api_name:
 - ReleaseExclusiveCpuSets
product: Windows
targetos: Windows
req.lib: Windowsapp.lib
req.dll: Gamemode.dll
req.irql: 
req.product: Internet Explorer 5
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



