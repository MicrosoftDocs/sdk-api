---
UID: NN:tapi3if.ITLegacyAddressMediaControl
title: ITLegacyAddressMediaControl (tapi3if.h)
author: windows-sdk-content
description: The ITLegacyAddressMediaControl interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the Address Object and can be created by calling QueryInterface on ITAddress.
old-location: tapi3\itlegacyaddressmediacontrol.htm
tech.root: Tapi
ms.assetid: 5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITLegacyAddressMediaControl, ITLegacyAddressMediaControl interface [TAPI 2.2], ITLegacyAddressMediaControl interface [TAPI 2.2],described, _tapi3_itlegacyaddressmediacontrol, tapi3.itlegacyaddressmediacontrol, tapi3if/ITLegacyAddressMediaControl
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
ms.custom: 19H1
---

# ITLegacyAddressMediaControl interface


## -description


The 
<b>ITLegacyAddressMediaControl</b> interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2">ITLegacyAddressMediaControl2</a> interface derives from the 
<b>ITLegacyAddressMediaControl</b> interface. 
<b>ITLegacyAddressMediaControl2</b> provides additional methods that allow the configuration of parameters related to line devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyAddressMediaControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITLegacyAddressMediaControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getdevconfig">GetDevConfig</a>
</td>
<td align="left" width="63%">
Gets pointer to device-specific array of configuration information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-getid">GetID</a>
</td>
<td align="left" width="63%">
Gets device identifier.

This method is intended for C/C++ applications only. There is no corresponding method available for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itlegacyaddressmediacontrol-setdevconfig">SetDevConfig</a>
</td>
<td align="left" width="63%">
Sets device-specific array of configuration information.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2">ITLegacyAddressMediaControl2</a>
 

 

