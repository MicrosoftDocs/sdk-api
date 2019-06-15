---
UID: NF:wcmconfig.ISettingsEngine.GetNamespace
title: ISettingsEngine::GetNamespace (wcmconfig.h)
author: windows-sdk-content
description: Opens an existing namespace as specified by the ISettingsIdentity parameter.
old-location: smi\isettingsengine_getnamespace.htm
tech.root: SMI
ms.assetid: 4f8193f5-9e9f-4819-aa2e-72b8623eca71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNamespace, GetNamespace method [SMI], GetNamespace method [SMI],ISettingsEngine interface, ISettingsEngine interface [SMI],GetNamespace method, ISettingsEngine.GetNamespace, ISettingsEngine::GetNamespace, smi.isettingsengine_getnamespace, wcmconfig/ISettingsEngine::GetNamespace
ms.topic: method
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
 - ISettingsEngine.GetNamespace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsEngine::GetNamespace


## -description


Opens an existing namespace as specified by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a> parameter.


## -parameters




### -param SettingsID [in]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsidentity">ISettingsIdentity</a> object that specifies an existing namespace to get.


### -param Access [in]

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/ne-wcmconfig-__midl___midl_itf_wcmconfig_0000_0000_0007">WcmNamespaceAccess</a> value that specifies the type of access, whether it is read-only or read and write access.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param NamespaceItem [out]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a> object that is the result of the get operation.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_USERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the store is not currently loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_NAMESPACENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the provided identity does not match a namespace registered in the store.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsengine">ISettingsEngine</a>
 

 

