---
UID: NN:wpcapi.IWPCProviderConfig
title: IWPCProviderConfig
author: windows-sdk-content
description: Exposes configuration methods that are implemented by third parties.
old-location: parcon\iwpcproviderconfig.htm
old-project: parcon
ms.assetid: 008786aa-72ef-4591-8826-01176d3e3fba
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IWPCProviderConfig, IWPCProviderConfig interface, IWPCProviderConfig interface,described, parcon.iwpcproviderconfig, wpcapi/IWPCProviderConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWPCProviderConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWPCProviderConfig interface


## -description


Exposes configuration methods that are implemented by third parties. Parental Controls uses the CLSID from the provider's ConfigCLSID registry details to call <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>. The <b>CLSCTX_LOCAL_SERVER</b> flag is used when creating an instance of the class.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWPCProviderConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWPCProviderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWPCProviderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2853259-4fc5-47e7-a77e-0ea4024ee00c">Configure</a>
</td>
<td align="left" width="63%">
Called for the current provider when you click a user tile in the Parental Controls Control Panel. This method allows for changes to the configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89d70aef-9bca-4984-99d1-082041257393">GetUserSummary</a>
</td>
<td align="left" width="63%">
Retrieves the information for each user by using the Parental Controls Control Panel.

</td>
</tr>
</table> 

