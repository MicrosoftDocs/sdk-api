---
UID: NN:mbnapi.IMbnMultiCarrierEvents
title: IMbnMultiCarrierEvents (mbnapi.h)
description: This interface is a notification interface used to handle asynchronous IMbnMultiCarrier method calls.helpviewer_keywords: ["IMbnMultiCarrierEvents","IMbnMultiCarrierEvents interface [Microsoft Broadband Networks]","IMbnMultiCarrierEvents interface [Microsoft Broadband Networks]","described","mbn.imbnmulticarrierevents","mbnapi/IMbnMultiCarrierEvents"]
old-location: mbn\imbnmulticarrierevents.htm
tech.root: mbn
ms.assetid: F7CAF21B-F487-4F35-806B-312B5246C1B2
ms.date: 12/05/2018
ms.keywords: IMbnMultiCarrierEvents, IMbnMultiCarrierEvents interface [Microsoft Broadband Networks], IMbnMultiCarrierEvents interface [Microsoft Broadband Networks],described, mbn.imbnmulticarrierevents, mbnapi/IMbnMultiCarrierEvents
f1_keywords:
- mbnapi/IMbnMultiCarrierEvents
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
- IMbnMultiCarrierEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnMultiCarrierEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This interface is a notification interface used to handle asynchronous <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnmulticarrier">IMbnMultiCarrier</a> method calls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnMultiCarrierEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnMultiCarrierEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnMultiCarrierEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-oncurrentcellularclasschange">OnCurrentCellularClassChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getcurrentcellularclass">GetCurrentCellularClass</a> operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-oninterfacecapabilitychange">OnInterfaceCapabilityChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation that updates the interface capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onpreferredproviderschange">OnPreferredProvidersChange</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-getpreferredproviders">GetPreferredProviders</a> operation and a change in a device's preferred provider list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onscannetworkcomplete">OnScanNetworkComplete</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-scannetwork">ScanNetwork</a> operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrierevents-onsethomeprovidercomplete">OnSetHomeProviderComplete</a>
</td>
<td align="left" width="63%">
This notification method is called by the Mobile Broadband service to indicate the completion of a <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnmulticarrier-sethomeprovider">SetHomeProvider</a> operation.

</td>
</tr>
</table> 

