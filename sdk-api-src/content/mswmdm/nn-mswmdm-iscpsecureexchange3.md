---
UID: NN:mswmdm.ISCPSecureExchange3
title: ISCPSecureExchange3 (mswmdm.h)
description: The ISCPSecureExchange3 interface extends ISCPSecureExchange2 by providing improved data exchange performance, and a transfer-complete callback method.
helpviewer_keywords: ["ISCPSecureExchange3","ISCPSecureExchange3 interface [windows Media Device Manager]","ISCPSecureExchange3 interface [windows Media Device Manager]","described","ISCPSecureExchange3Interface","mswmdm/ISCPSecureExchange3","wmdm.iscpsecureexchange3"]
old-location: wmdm\iscpsecureexchange3.htm
tech.root: WMDM
ms.assetid: 2617a6af-c91d-4416-8bef-fe69404e7c3f
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange3, ISCPSecureExchange3 interface [windows Media Device Manager], ISCPSecureExchange3 interface [windows Media Device Manager],described, ISCPSecureExchange3Interface, mswmdm/ISCPSecureExchange3, wmdm.iscpsecureexchange3
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
 - ISCPSecureExchange3
 - mswmdm/ISCPSecureExchange3
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
 - ISCPSecureExchange3
---

# ISCPSecureExchange3 interface


## -description

The <b>ISCPSecureExchange3</b> interface extends <b>ISCPSecureExchange2</b> by providing improved data exchange performance, and a transfer-complete callback method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureExchange3</b> interface inherits from <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2">ISCPSecureExchange2</a>. <b>ISCPSecureExchange3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureExchange3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/WMDM/iscpsecureexchange3--getobjectdataonclearchannel">GetObjectDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Retrieves the object data on a clear channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercompletefordevice">TransferCompleteForDevice</a>
</td>
<td align="left" width="63%">
Indicates that the data transfer has completed for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel">TransferContainerDataOnClearChannel</a>
</td>
<td align="left" width="63%">
Transfers the container data on a clear channel.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2">ISCPSecureExchange2 Interface</a>



<a href="/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>