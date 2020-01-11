---
UID: NN:mbnapi.IMbnVendorSpecificOperation
title: IMbnVendorSpecificOperation (mbnapi.h)
description: Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.
old-location: mbn\imbnvendorspecificoperation.htm
tech.root: mbn
ms.assetid: cbc905f6-c5ac-4c6a-9021-4ec00b938bb2
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificOperation, IMbnVendorSpecificOperation interface [Microsoft Broadband Networks], IMbnVendorSpecificOperation interface [Microsoft Broadband Networks],described, mbn.imbnvendorspecificoperation, mbnapi/IMbnVendorSpecificOperation
f1_keywords:
- mbnapi/IMbnVendorSpecificOperation
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
- IMbnVendorSpecificOperation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnVendorSpecificOperation interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnVendorSpecificOperation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnVendorSpecificOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnVendorSpecificOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnvendorspecificoperation-setvendorspecific">SetVendorSpecific</a>
</td>
<td align="left" width="63%">
Send a request to the miniport driver.

</td>
</tr>
</table> 


## -remarks



The calling application can acquire this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.



