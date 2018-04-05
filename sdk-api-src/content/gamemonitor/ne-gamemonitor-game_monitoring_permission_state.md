---
UID: NE:gamemonitor.GAME_MONITORING_PERMISSION_STATE
title: GAME_MONITORING_PERMISSION_STATE
author: windows-driver-content
description: Indicates whether game monitoring is disabled.
old-location: anticheat\game_monitoring_permission_state.htm
old-project: anticheat
ms.assetid: A31B8F98-AE71-4414-8975-8A1B6D437EBC
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GAME_MONITORING_ALLOWED, GAME_MONITORING_DENIED_BY_SYSTEM, GAME_MONITORING_DENIED_BY_USER, GAME_MONITORING_NOT_SUPPORTED, GAME_MONITORING_PERMISSION_STATE, GAME_MONITORING_PERMISSION_STATE enumeration, anticheat.game_monitoring_permission_state, gamemonitor/GAME_MONITORING_ALLOWED, gamemonitor/GAME_MONITORING_DENIED_BY_SYSTEM, gamemonitor/GAME_MONITORING_DENIED_BY_USER, gamemonitor/GAME_MONITORING_NOT_SUPPORTED, gamemonitor/GAME_MONITORING_PERMISSION_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
-	HeaderDef
api_location:
-	gamemonitor.h
api_name:
-	GAME_MONITORING_PERMISSION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxsutility.dll
req.irql: 
req.product: Internet Explorer 5
---

# GAME_MONITORING_PERMISSION_STATE enumeration


## -description


<div class="alert"><b>Warning</b>  This API is intended for use only in a small number of specific and limited scenarios. Please work with your Microsoft account manager if you’ve been directed to use this API.</div><div> </div>Indicates whether game monitoring is disabled.


## -enum-fields




### -field GAME_MONITORING_ALLOWED

The user has enabled game monitoring.


### -field GAME_MONITORING_DENIED_BY_USER

The user has disabled game monitoring.


### -field GAME_MONITORING_DENIED_BY_SYSTEM

The device has disabled game monitoring (for example, due to a group policy).


### -field GAME_MONITORING_NOT_SUPPORTED

The device doesn't support game monitoring (for example, it isn't a desktop).


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

This enumeration is returned by the <a href="https://msdn.microsoft.com/34C56371-9592-4940-886C-8B8CB5E294F2">GetGameMonitoringPermissionState</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e86f4d72-c29f-4720-beec-da57ba6617bc">TruePlay</a>
 

 

