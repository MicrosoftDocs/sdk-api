---
UID: NN:wcmconfig.ISettingsEngine
title: ISettingsEngine (wcmconfig.h)
description: The central interface for opening namespaces and controlling how they are opened.
old-location: smi\isettingsengine.htm
tech.root: SMI
ms.assetid: ba816a00-e238-4dbd-a09a-ad4e191d9c4e
ms.date: 12/05/2018
ms.keywords: ISettingsEngine, ISettingsEngine interface [SMI], ISettingsEngine interface [SMI],described, smi.isettingsengine, wcmconfig/ISettingsEngine
ms.topic: interface
f1_keywords:
- wcmconfig/ISettingsEngine
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
- ISettingsEngine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsEngine interface


## -description


The central interface for opening namespaces and controlling how they are opened.Unless otherwise specified, all methods return an HRESULT value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsEngine</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-applysettingscontext">ApplySettingsContext</a>
</td>
<td align="left" width="63%">
 Applies the context to the engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-createsettingscontext">CreateSettingsContext</a>
</td>
<td align="left" width="63%">
 Creates a settings context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-createsettingsidentity">CreateSettingsIdentity</a>
</td>
<td align="left" width="63%">
Creates an empty settings identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-createtargetinfo">CreateTargetInfo</a>
</td>
<td align="left" width="63%">
 Creates an empty target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-geterrordescription">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves the message string associated with an HResult value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getnamespace">GetNamespace</a>
</td>
<td align="left" width="63%">
Opens an existing namespace that contains the settings and metadata to access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getnamespace">GetNamespaces</a>
</td>
<td align="left" width="63%">
Retrieves a dictionary of installed namespaces, that the current user owns, and all shared namespaces. Use an identifier from the collection to open a namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-getstorestatus">GetStoreStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the schema store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-gettargetinfo">GetTargetInfo</a>
</td>
<td align="left" width="63%">
 Gets the current offline target for engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-loadstore">LoadStore</a>
</td>
<td align="left" width="63%">
Initializes and loads the schema store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-registernamespace">RegisterNamespace</a>
</td>
<td align="left" width="63%">
Registers a namespace from the stream and upgrades the setting values from the older version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-settargetinfo">SetTargetInfo</a>
</td>
<td align="left" width="63%">
 Sets the current offline target for engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-unloadstore">UnloadStore</a>
</td>
<td align="left" width="63%">
Unloads the schema store and frees resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsengine-unregisternamespace">UnregisterNamespace</a>
</td>
<td align="left" width="63%">
Unregisters an existing namespace.

</td>
</tr>
</table> 

