---
UID: NN:tapi3if.ITLegacyAddressMediaControl
title: ITLegacyAddressMediaControl
author: windows-sdk-content
description: The ITLegacyAddressMediaControl interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the Address Object and can be created by calling QueryInterface on ITAddress.
old-location: tapi3\itlegacyaddressmediacontrol.htm
tech.root: TAPI
ms.assetid: 5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITLegacyAddressMediaControl, ITLegacyAddressMediaControl interface [TAPI 2.2], ITLegacyAddressMediaControl interface [TAPI 2.2],described, _tapi3_itlegacyaddressmediacontrol, tapi3.itlegacyaddressmediacontrol, tapi3if/ITLegacyAddressMediaControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyAddressMediaControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLegacyAddressMediaControl interface


## -description


The 
<b>ITLegacyAddressMediaControl</b> interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>.

The 
<a href="https://msdn.microsoft.com/38e5f1ba-b31e-47c9-a24a-2e4d37a0961b">ITLegacyAddressMediaControl2</a> interface derives from the 
<b>ITLegacyAddressMediaControl</b> interface. 
<b>ITLegacyAddressMediaControl2</b> provides additional methods that allow the configuration of parameters related to line devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyAddressMediaControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITLegacyAddressMediaControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyAddressMediaControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed8cc556-31a5-4725-92fe-1f78c16aadcd">GetDevConfig</a>
</td>
<td align="left" width="63%">
Gets pointer to device-specific array of configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4fdde49-0867-4967-b975-f43bd9f6adc4">GetID</a>
</td>
<td align="left" width="63%">
Gets device identifier.

This method is intended for C/C++ applications only. There is no corresponding method available for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c5fe0ab-8a03-41db-994b-9786782cf7c1">SetDevConfig</a>
</td>
<td align="left" width="63%">
Sets device-specific array of configuration information.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/38e5f1ba-b31e-47c9-a24a-2e4d37a0961b">ITLegacyAddressMediaControl2</a>
 

 

