---
UID: NN:mbnapi.IMbnDeviceServicesManager
title: IMbnDeviceServicesManager (mbnapi.h)
author: windows-sdk-content
description: Provides access to IMbnDeviceServicesContext objects and Mobile Broadband device service notifications.
old-location: mbn\imbndeviceservicesmanager.htm
tech.root: mbn
ms.assetid: 6CFF2275-0649-4009-84F2-0657B2FF281C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesManager, IMbnDeviceServicesManager interface [Microsoft Broadband Networks], IMbnDeviceServicesManager interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicesmanager, mbnapi/IMbnDeviceServicesManager
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnDeviceServicesManager"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
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
 - IMbnDeviceServicesManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnDeviceServicesManager interface


## -description


Provides access to <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> objects and Mobile Broadband device service notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceServicesManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnDeviceServicesManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesmanager-getdeviceservicescontext">GetDeviceServicesContext</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> interface for a specific Mobile Broadband device

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.<ol>
<li>Get an <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on an <b>IMbnDeviceServicesManager</b> object.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a> on the returned interface and pass IID_IMbnDeviceServicesEvents to RIID.</li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a> on the returned connection point and pass a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on an object that implements <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a> to PUNK.</li>
</ol>


Notifications can be terminated by calling <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a> on the connection point returned in step 2.

For sample code that registers COM notifications, see the Client section of the <a href="https://msdn.microsoft.com/magazine/msdn-magazine-issues">COM Connection Points article</a>.



