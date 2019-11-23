---
UID: NN:mswmdm.IWMDMDeviceSession
title: IWMDMDeviceSession (mswmdm.h)

description: The IWMDMDeviceSession interface improves the efficiency of device operations by bundling multiple operations into one session.
old-location: wmdm\iwmdmdevicesession.htm
tech.root: WMDM
ms.assetid: 37a57fbe-d0f8-44ee-b6c5-2c6a34e12f2b

ms.date: 12/05/2018
ms.keywords: IWMDMDeviceSession, IWMDMDeviceSession interface [windows Media Device Manager], IWMDMDeviceSession interface [windows Media Device Manager],described, IWMDMDeviceSessionInterface, mswmdm/IWMDMDeviceSession, wmdm.iwmdmdevicesession
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMDeviceSession"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMDeviceSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDeviceSession interface


## -description



The <b>IWMDMDeviceSession</b> interface improves the efficiency of device operations by bundling multiple operations into one session. Using a single session allows Windows Media Device Manager to handle various operations, such as acquiring a device certificate, once over several operations.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDeviceSession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMDeviceSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDeviceSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-beginsession">BeginSession</a>
</td>
<td align="left" width="63%">
Begins a device session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevicesession-endsession">EndSession</a>
</td>
<td align="left" width="63%">
Ends a device session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

