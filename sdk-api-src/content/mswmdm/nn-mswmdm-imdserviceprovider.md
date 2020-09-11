---
UID: NN:mswmdm.IMDServiceProvider
title: IMDServiceProvider (mswmdm.h)
description: The IMDServiceProvider interface is the initial interface that Windows Media Device Manager uses to connect to your service provider.
helpviewer_keywords: ["IMDServiceProvider","IMDServiceProvider interface [windows Media Device Manager]","IMDServiceProvider interface [windows Media Device Manager]","described","IMDServiceProviderInterface","mswmdm/IMDServiceProvider","wmdm.imdserviceprovider"]
old-location: wmdm\imdserviceprovider.htm
tech.root: WMDM
ms.assetid: 803b6cc5-2cb2-42ad-a92c-05f098cbe8ae
ms.date: 12/05/2018
ms.keywords: IMDServiceProvider, IMDServiceProvider interface [windows Media Device Manager], IMDServiceProvider interface [windows Media Device Manager],described, IMDServiceProviderInterface, mswmdm/IMDServiceProvider, wmdm.imdserviceprovider
req.header: mswmdm.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDServiceProvider
 - mswmdm/IMDServiceProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDServiceProvider
---

# IMDServiceProvider interface


## -description

The <b>IMDServiceProvider</b> interface is the initial interface that Windows Media Device Manager uses to connect to your service provider. Using this interface, Windows Media Device Manager can enumerate and communicate with the all media devices supported by a particular service provider. The <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2</a> interface can be implemented to create devices by using the device path.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDServiceProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDServiceProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDServiceProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices">EnumDevices</a>
</td>
<td align="left" width="63%">
Enumerates the installed physical or software devices that are currently attached and are known by the service provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-getdevicecount">GetDeviceCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of media devices that are currently attached and are known by the service provider.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>

