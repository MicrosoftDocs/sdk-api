---
UID: NN:wcmconfig.ISettingsNamespace
title: ISettingsNamespace (wcmconfig.h)
author: windows-sdk-content
description: Performs operations to set, retrieve, and validate settings, and save changes for a namespace instance.
old-location: smi\isettingsnamespace.htm
tech.root: SMI
ms.assetid: a5d7b9ff-eb6f-40be-b246-17189cad92be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISettingsNamespace, ISettingsNamespace interface [SMI], ISettingsNamespace interface [SMI],described, smi.isettingsnamespace, wcmconfig/ISettingsNamespace
ms.topic: interface
f1_keywords: 
 - "wcmconfig/ISettingsNamespace"
dev_langs:
 - c++
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsNamespace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsNamespace interface


## -description


Performs operations to set, retrieve, and validate settings, and save changes for a namespace instance.

To retrieve an <b>ISettingsNamespace</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getnamespace">ISettingsEngine::GetNamespace</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsNamespace</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsNamespace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsNamespace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-createsettingbypath">CreateSettingByPath</a>
</td>
<td align="left" width="63%">
Creates a setting object specified by its path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets the value of an attribute of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-getidentity">GetIdentity</a>
</td>
<td align="left" width="63%">
Retrieves the identity of the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-getsettingbypath">GetSettingByPath</a>
</td>
<td align="left" width="63%">
Retrieves a  setting by specifying its path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-removesettingbypath">RemoveSettingByPath</a>
</td>
<td align="left" width="63%">
Removes the setting object specified by a path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-save">Save</a>
</td>
<td align="left" width="63%">
Updates the settings namespace to persistent and visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsnamespace-settings">Settings</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the top-level settings for the namespace.

</td>
</tr>
</table> 

