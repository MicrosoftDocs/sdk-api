---
UID: NF:wpcapi.IWPCProviderConfig.Configure
title: IWPCProviderConfig::Configure
author: windows-sdk-content
description: Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.
old-location: parcon\iwpcproviderconfig_configure.htm
tech.root: parcon
ms.assetid: a2853259-4fc5-47e7-a77e-0ea4024ee00c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Configure, Configure method, Configure method,IWPCProviderConfig interface, IWPCProviderConfig interface,Configure method, IWPCProviderConfig.Configure, IWPCProviderConfig::Configure, parcon.iwpcproviderconfig_configure, wpcapi/IWPCProviderConfig::Configure
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderConfig.Configure
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWPCProviderConfig::Configure


## -description


Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.


## -parameters




### -param hWnd [in]

A handle to the parent window.


### -param bstrSID [in]

A string that contains the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the user to configure.


## -returns



If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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




<a href="https://msdn.microsoft.com/008786aa-72ef-4591-8826-01176d3e3fba">IWPCProviderConfig</a>
 

 

