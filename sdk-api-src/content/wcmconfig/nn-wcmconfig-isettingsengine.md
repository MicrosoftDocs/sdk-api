---
UID: NN:wcmconfig.ISettingsEngine
title: ISettingsEngine
author: windows-sdk-content
description: The central interface for opening namespaces and controlling how they are opened.
old-location: smi\isettingsengine.htm
old-project: SMI
ms.assetid: ba816a00-e238-4dbd-a09a-ad4e191d9c4e
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISettingsEngine, ISettingsEngine interface [SMI], ISettingsEngine interface [SMI],described, smi.isettingsengine, wcmconfig/ISettingsEngine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsEngine
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsEngine interface


## -description


The central interface for opening namespaces and controlling how they are opened.


Unless otherwise specified, all methods return an HRESULT value.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsEngine</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/459a97fb-e5fb-42a5-998d-84631fec2e6f">ApplySettingsContext</a>
</td>
<td align="left" width="63%">
 Applies the context to the engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9fe2c24-f696-4726-8e67-07280c8e8a3e">CreateSettingsContext</a>
</td>
<td align="left" width="63%">
 Creates a settings context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b48e6784-5565-4809-873e-cadedce57743">CreateSettingsIdentity</a>
</td>
<td align="left" width="63%">
Creates an empty settings identity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3d31643-c606-4fc1-96a8-cf5cb26bcf3f">CreateTargetInfo</a>
</td>
<td align="left" width="63%">
 Creates an empty target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a1ac3eb-c2d5-4a23-928e-51ef1a52ad73">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Retrieves the message string associated with an HResult value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f8193f5-9e9f-4819-aa2e-72b8623eca71">GetNamespace</a>
</td>
<td align="left" width="63%">
Opens an existing namespace that contains the settings and metadata to access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f8193f5-9e9f-4819-aa2e-72b8623eca71">GetNamespaces</a>
</td>
<td align="left" width="63%">
Retrieves a dictionary of installed namespaces, that the current user owns, and all shared namespaces. Use an identifier from the collection to open a namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/212299b4-d7b3-4a11-b75e-7e752bb91932">GetStoreStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the schema store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e14644b-84bc-48eb-8d8c-d6290db72dea">GetTargetInfo</a>
</td>
<td align="left" width="63%">
 Gets the current offline target for engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd255730-1c42-41a3-b274-e2abe53f210e">LoadStore</a>
</td>
<td align="left" width="63%">
Initializes and loads the schema store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b9ffba8-b2b7-469e-96d2-78b086987fae">RegisterNamespace</a>
</td>
<td align="left" width="63%">
Registers a namespace from the stream and upgrades the setting values from the older version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a33a0155-0533-4450-9e03-2688ad776a1a">SetTargetInfo</a>
</td>
<td align="left" width="63%">
 Sets the current offline target for engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10c0e5c7-41df-4ebb-86be-0c2c6e013849">UnloadStore</a>
</td>
<td align="left" width="63%">
Unloads the schema store and frees resources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7254f87-fdf8-4b51-9a06-e593490cd3c5">UnregisterNamespace</a>
</td>
<td align="left" width="63%">
Unregisters an existing namespace.

</td>
</tr>
</table> 

