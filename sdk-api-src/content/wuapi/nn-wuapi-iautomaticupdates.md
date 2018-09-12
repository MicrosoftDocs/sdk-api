---
UID: NN:wuapi.IAutomaticUpdates
title: IAutomaticUpdates
author: windows-sdk-content
description: Contains the functionality of Automatic Updates.
old-location: wua\iautomaticupdates.htm
tech.root: wua_sdk
ms.assetid: b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IAutomaticUpdates, IAutomaticUpdates interface [Windows Update Agent], IAutomaticUpdates interface [Windows Update Agent],described, wua.iautomaticupdates, wuapi/IAutomaticUpdates
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutomaticUpdates interface


## -description


Contains the functionality of Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdates</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IAutomaticUpdates</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAutomaticUpdates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef40cd57-eab3-4ccf-a574-ab5237565e5b">DetectNow</a>
</td>
<td align="left" width="63%">
Begins automatic updating if it has not already started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dd80943-f9d6-4179-8b02-3a03b5ba3636">EnableService</a>
</td>
<td align="left" width="63%">
Enables all the components that Automatic Updates requires.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42985fdf-b3b3-43f0-addb-478298bd8ebd">Pause</a>
</td>
<td align="left" width="63%">
Pauses automatic updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aabfb89-89e2-450e-bfe6-62a48f93746f">Resume</a>
</td>
<td align="left" width="63%">
Restarts automatic updating if it is paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da153799-9414-4e8e-aed4-96e0fff9ca88">ShowSettingsDialog</a>
</td>
<td align="left" width="63%">
Displays a dialog box that contains settings for Automatic Updates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdates</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6d07ed15-f891-47c4-b4a6-2e57207dbdb3">ServiceEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether all the components that Automatic Updates requires are available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4b64d8bd-98bb-4d3a-9e90-2c6500c8614b">Settings</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the configuration settings for Automatic Updates.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the AutomaticUpdates coclass. Use the Microsoft.Update.AutoUpdate program identifier to create the object.




## -see-also




<a href="https://msdn.microsoft.com/9cb09bb2-5532-446b-9441-0987d50c6228">IAutomaticUpdates2</a>
 

 

