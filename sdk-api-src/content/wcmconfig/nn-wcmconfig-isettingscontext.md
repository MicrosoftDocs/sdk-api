---
UID: NN:wcmconfig.ISettingsContext
title: ISettingsContext (wcmconfig.h)
description: An interface to a backing store that is used to store setting changes made through the other SMI APIs, and provides operations to serialize to and deserialize from a representation.
helpviewer_keywords: ["ISettingsContext","ISettingsContext interface [SMI]","ISettingsContext interface [SMI]","described","smi.isettingscontext","wcmconfig/ISettingsContext"]
old-location: smi\isettingscontext.htm
tech.root: SMI
ms.assetid: 29f43c3f-57bf-4208-a0bf-9b4414795a59
ms.date: 12/05/2018
ms.keywords: ISettingsContext, ISettingsContext interface [SMI], ISettingsContext interface [SMI],described, smi.isettingscontext, wcmconfig/ISettingsContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsContext
 - wcmconfig/ISettingsContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsContext
---

# ISettingsContext interface


## -description

An interface to a backing store that is used to store setting changes made through the other SMI APIs, and provides operations to serialize to and deserialize from a representation.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-deserialize">Deserialize</a>
</td>
<td align="left" width="63%">
 Deserializes the data in the provided stream into this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-getnamespaces">GetNamespaces</a>
</td>
<td align="left" width="63%">
Gets the namespaces that exist in the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-getstoredsettings">GetStoredSettings</a>
</td>
<td align="left" width="63%">
Gets the stored setting changes from the context for the given namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-getuserdata">GetUserData</a>
</td>
<td align="left" width="63%">
Gets a user-defined piece of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-revertsetting">RevertSetting</a>
</td>
<td align="left" width="63%">
Reverts a setting in the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the data in this context into the provided stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingscontext-setuserdata">SetUserData</a>
</td>
<td align="left" width="63%">
Sets a user-defined piece of data.

</td>
</tr>
</table>

