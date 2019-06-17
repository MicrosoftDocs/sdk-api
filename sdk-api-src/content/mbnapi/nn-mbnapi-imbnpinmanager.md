---
UID: NN:mbnapi.IMbnPinManager
title: IMbnPinManager (mbnapi.h)
author: windows-sdk-content
description: Provides important details about the device PIN.
old-location: mbn\imbnpinmanager.htm
tech.root: mbn
ms.assetid: b5cfabc7-81f8-4ea0-b6f4-5de011320f0b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnPinManager, IMbnPinManager interface [Microsoft Broadband Networks], IMbnPinManager interface [Microsoft Broadband Networks],described, mbn.imbnpinmanager, mbnapi/IMbnPinManager
ms.topic: interface
f1_keywords: ["mbnapi/IMbnPinManager"]
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnPinManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnPinManager interface


## -description


Provides important details about the device PIN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPinManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnPinManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnPinManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpin">GetPin</a>
</td>
<td align="left" width="63%">
Gets the device PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinlist">GetPinList</a>
</td>
<td align="left" width="63%">
Gets a list of different PIN types supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a>
</td>
<td align="left" width="63%">
Gets the current PIN state of the device.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.



