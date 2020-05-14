---
UID: NN:mbnapi.IMbnMultiCarrier
title: IMbnMultiCarrier (mbnapi.h)
description: This interface exposes the multi-carrier functionality of a capable Mobile Broadband device.helpviewer_keywords: ["IMbnMultiCarrier","IMbnMultiCarrier interface [Microsoft Broadband Networks]","IMbnMultiCarrier interface [Microsoft Broadband Networks]","described","mbn.imbnmulticarrier","mbnapi/IMbnMultiCarrier"]
old-location: mbn\imbnmulticarrier.htm
tech.root: mbn
ms.assetid: E40517CE-3169-4F20-A572-EDBC8FEC2862
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrier, IMbnMultiCarrier interface [Microsoft Broadband Networks], IMbnMultiCarrier interface [Microsoft Broadband Networks],described, mbn.imbnmulticarrier, mbnapi/IMbnMultiCarrier
f1_keywords:
- mbnapi/IMbnMultiCarrier
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
- mbnapi.h
api_name:
- IMbnMultiCarrier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnMultiCarrier interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This interface exposes the multi-carrier functionality of a capable Mobile Broadband device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnMultiCarrier</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnMultiCarrier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnMultiCarrier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getcurrentcellularclass">GetCurrentCellularClass</a>
</td>
<td align="left" width="63%">
Gets the current cellular classes for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getpreferredproviders">GetPreferredProviders</a>
</td>
<td align="left" width="63%">
Gets the list of subscribed providers visible in the current area for a multi-carrier device minus the current registered provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getsupportedcellularclasses">GetSupportedCellularClasses</a>
</td>
<td align="left" width="63%">
Gets the list of supported cellular classes for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getvisibleproviders">GetVisibleProviders</a>
</td>
<td align="left" width="63%">
Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-scannetwork">ScanNetwork</a>
</td>
<td align="left" width="63%">
Scans the network to get a list of visible providers for a multi-carrier device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a>
</td>
<td align="left" width="63%">
Updates the home provider for a multi-carrier device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/ne-mbnapi-mbn_ctrl_caps">MBN_CTRL_CAPS</a>
 

 

