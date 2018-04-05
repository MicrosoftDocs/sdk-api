---
UID: NF:gamemonitor.GetGameMonitoringPermissionState
title: GetGameMonitoringPermissionState function
author: windows-driver-content
description: Gets the current game monitoring permission state of the device.
old-location: anticheat\getgamemonitoringpermissionstate.htm
old-project: anticheat
ms.assetid: 34C56371-9592-4940-886C-8B8CB5E294F2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetGameMonitoringPermissionState, GetGameMonitoringPermissionState function, anticheat.getgamemonitoringpermissionstate, gamemonitor/GetGameMonitoringPermissionState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gamemonitor.h
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
req.typenames: GAME_MONITORING_PERMISSION_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gamemonitor.dll
api_name:
-	GetGameMonitoringPermissionState
product: Windows
targetos: Windows
req.lib: Windowsapp.lib
req.dll: Gamemonitor.dll
req.irql: 
req.product: Internet Explorer 5
---

# GetGameMonitoringPermissionState function


## -description


<div class="alert"><b>Warning</b>  This API is intended for use only in a small number of specific and limited scenarios. Please work with your Microsoft account manager if you’ve been directed to use this API.</div><div> </div>Gets the current game monitoring permission state of the device. This API has no UX.


## -parameters




### -param permissionState [out]

The current game monitoring permission state.


## -returns



This function does not return a value.




## -remarks



This is a Win32 API that's only supported in UWP desktop apps. It also requires the <b>gameMonitor</b> and <b>protectedApp</b> restricted capabilities, which you can select by opening <b>Package.appxmanifest</b> in Visual Studio and navigating to the <b>Capabilities</b> tab. Alternatively, you can edit the file's code directly:

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
	&lt;Capabilities&gt;
		&lt;rescap:Capability Name="gameMonitor" /&gt;
		&lt;rescap:Capability Name="protectedApp" /&gt;
	&lt;/Capabilities&gt;
	...
&lt;/Package&gt;</pre>
</td>
</tr>
</table></span></div>
These capabilities are granted on a per-title basis; contact your account manager for more information.

Use this API to determine whether or not the current PC has permission to collect and share data regarding any detected cheat behaviors. If <i>permissionState</i> is not equal to <b>GAME_MONITORING_ALLOWED</b>, no data will be shared from this system.




## -see-also




<a href="https://msdn.microsoft.com/A31B8F98-AE71-4414-8975-8A1B6D437EBC">GAME_MONITORING_PERMISSION_STATE enumeration</a>



<a href="https://msdn.microsoft.com/e86f4d72-c29f-4720-beec-da57ba6617bc">TruePlay</a>
 

 

