---
UID: NN:wuapi.IInstallationResult
title: IInstallationResult
author: windows-driver-content
description: Represents the result of an installation or uninstallation.
old-location: wua\iinstallationresult.htm
old-project: Wua_Sdk
ms.assetid: 453945d7-11a3-4237-b1c8-928194be558d
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IInstallationResult, IInstallationResult interface [Windows Update Agent], IInstallationResult interface [Windows Update Agent], described, wua.iinstallationresult, wuapi/IInstallationResult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IInstallationResult
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IInstallationResult interface


## -description


Represents the result of an installation or uninstallation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationResult</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IInstallationResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInstallationResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51d84e9e-9d92-43c9-af13-f833c3f3d631">GetUpdateResult</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/6c27d691-d9b1-41ce-b3e8-dd2574c19b8b">IUpdateInstallationResult</a> interface that contains the installation results for a specified update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/75178661-3b21-4d21-971c-93362a2cc287">HResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <b>HRESULT</b> of the exception, if any, that is raised during the installation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a865933-53f7-4d3e-88cf-088acedeed02">RebootRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/09454585-ce1e-41e9-8c8a-8a5cffb94388">ResultCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/02d3442e-d098-42b6-b1b1-cc2d1a815fa4">OperationResultCode</a> value that specifies the result of an operation on an update.

</td>
</tr>
</table> 

