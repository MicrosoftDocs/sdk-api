---
UID: NN:wuapi.IAutomaticUpdates
title: IAutomaticUpdates (wuapi.h)
description: Contains the functionality of Automatic Updates.
old-location: wua\iautomaticupdates.htm
tech.root: Wua_Sdk
ms.assetid: b5f05e2a-ad60-4d4c-8bdd-1c03df3d508d
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdates, IAutomaticUpdates interface [Windows Update Agent], IAutomaticUpdates interface [Windows Update Agent],described, wua.iautomaticupdates, wuapi/IAutomaticUpdates
f1_keywords:
- wuapi/IAutomaticUpdates
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutomaticUpdates interface


## -description


Contains the functionality of Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdates</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAutomaticUpdates</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-detectnow">DetectNow</a>
</td>
<td align="left" width="63%">
Begins automatic updating if it has not already started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-enableservice">EnableService</a>
</td>
<td align="left" width="63%">
Enables all the components that Automatic Updates requires.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses automatic updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-resume">Resume</a>
</td>
<td align="left" width="63%">
Restarts automatic updating if it is paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog">ShowSettingsDialog</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled">ServiceEnabled</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdates-get_settings">Settings</a>


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




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdates2">IAutomaticUpdates2</a>
 

 

