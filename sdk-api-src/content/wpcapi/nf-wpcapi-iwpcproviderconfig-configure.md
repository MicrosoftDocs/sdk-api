---
UID: NF:wpcapi.IWPCProviderConfig.Configure
title: IWPCProviderConfig::Configure (wpcapi.h)
description: Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.
helpviewer_keywords: ["Configure","Configure method","Configure method","IWPCProviderConfig interface","IWPCProviderConfig interface","Configure method","IWPCProviderConfig.Configure","IWPCProviderConfig::Configure","parcon.iwpcproviderconfig_configure","wpcapi/IWPCProviderConfig::Configure"]
old-location: parcon\iwpcproviderconfig_configure.htm
tech.root: parcon
ms.assetid: a2853259-4fc5-47e7-a77e-0ea4024ee00c
ms.date: 12/05/2018
ms.keywords: Configure, Configure method, Configure method,IWPCProviderConfig interface, IWPCProviderConfig interface,Configure method, IWPCProviderConfig.Configure, IWPCProviderConfig::Configure, parcon.iwpcproviderconfig_configure, wpcapi/IWPCProviderConfig::Configure
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wpcprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWPCProviderConfig::Configure
 - wpcapi/IWPCProviderConfig::Configure
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderConfig.Configure
---

# IWPCProviderConfig::Configure


## -description

Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.

## -parameters

### -param hWnd [in]

A handle to the parent window.

### -param bstrSID [in]

A string that contains the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the user to configure.

## -returns

If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Allows the provider to not handle the configuration user interface and instead to rely on the in-box Parental Controls configuration user interface.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwpcproviderconfig">IWPCProviderConfig</a>