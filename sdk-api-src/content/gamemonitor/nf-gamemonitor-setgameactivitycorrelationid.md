---
UID: NF:gamemonitor.SetGameActivityCorrelationId
title: SetGameActivityCorrelationId function
author: windows-driver-content
description: Allows the game to set a correlation ID that you can use to correlate the game monitoring logs with your own gaming session logs.
old-location: anticheat\setgameactivitycorrelationid.htm
old-project: anticheat
ms.assetid: 7E5F97A1-66C0-4130-9D50-656E12A48151
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetGameActivityCorrelationId, SetGameActivityCorrelationId function, anticheat.setgameactivitycorrelationid, gamemonitor/SetGameActivityCorrelationId
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
-	SetGameActivityCorrelationId
product: Windows
targetos: Windows
req.lib: Windowsapp.lib
req.dll: Gamemonitor.dll
req.irql: 
req.product: Internet Explorer 5
---

# SetGameActivityCorrelationId function


## -description


<div class="alert"><b>Warning</b>  This API is intended for use only in a small number of specific and limited scenarios. Please work with your Microsoft account manager if you’ve been directed to use this API.</div><div> </div>Allows the game to set a correlation ID that you can use to correlate the game monitoring logs with your own gaming session logs.


## -parameters




### -param id [in]

The correlation ID.


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




## -see-also




<a href="https://msdn.microsoft.com/e86f4d72-c29f-4720-beec-da57ba6617bc">TruePlay</a>
 

 

