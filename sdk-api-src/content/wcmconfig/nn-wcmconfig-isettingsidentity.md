---
UID: NN:wcmconfig.ISettingsIdentity
title: ISettingsIdentity (wcmconfig.h)
description: Identifies a namespace to open or use.
helpviewer_keywords: ["ISettingsIdentity","ISettingsIdentity interface [SMI]","ISettingsIdentity interface [SMI]","described","smi.isettingsidentity","wcmconfig/ISettingsIdentity"]
old-location: smi\isettingsidentity.htm
tech.root: SMI
ms.assetid: aa9d5604-5b94-47d9-9e68-d708a656a5ea
ms.date: 12/05/2018
ms.keywords: ISettingsIdentity, ISettingsIdentity interface [SMI], ISettingsIdentity interface [SMI],described, smi.isettingsidentity, wcmconfig/ISettingsIdentity
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
 - ISettingsIdentity
 - wcmconfig/ISettingsIdentity
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
 - ISettingsIdentity
---

# ISettingsIdentity interface


## -description

Identifies a namespace to open or use.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsIdentity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsIdentity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsIdentity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsidentity-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets the identity attribute for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsidentity-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the identity flags for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsidentity-setattribute">SetAttribute</a>
</td>
<td align="left" width="63%">
Sets the identity attribute for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsidentity-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
 Sets the identity flags for a setting.

</td>
</tr>
</table>

