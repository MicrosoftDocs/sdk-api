---
UID: NN:mbnapi.IMbnDeviceServicesContext
title: IMbnDeviceServicesContext (mbnapi.h)
description: Allows for enumerating and retrieving Mobile Broadband device objects on the system.helpviewer_keywords: ["IMbnDeviceServicesContext","IMbnDeviceServicesContext interface [Microsoft Broadband Networks]","IMbnDeviceServicesContext interface [Microsoft Broadband Networks]","described","mbn.imbndeviceservicescontext","mbnapi/IMbnDeviceServicesContext"]
old-location: mbn\imbndeviceservicescontext.htm
tech.root: mbn
ms.assetid: 0B97FCCD-0A90-4FA2-9122-B00BD3F1A033
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesContext, IMbnDeviceServicesContext interface [Microsoft Broadband Networks], IMbnDeviceServicesContext interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicescontext, mbnapi/IMbnDeviceServicesContext
f1_keywords:
- mbnapi/IMbnDeviceServicesContext
dev_langs:
- c++
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
- IMbnDeviceServicesContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnDeviceServicesContext interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Allows for enumerating and retrieving Mobile Broadband device objects on the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceServicesContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnDeviceServicesContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-enumeratedeviceservices">EnumerateDeviceServices</a>
</td>
<td align="left" width="63%">
Gets the list of supported device services by the Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-getdeviceservice">GetDeviceService</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> object that can be used for communicating with a device service on the Mobile Broadband device.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesContext</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxcommandsize">MaxCommandSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length, in bytes, of data that can be associated with a device service <b>SET</b> or <b>QUERY</b> command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-get_maxdatasize">MaxDataSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length, in bytes, of data that can be written to or read from a device service session.

</td>
</tr>
</table> 


## -remarks



<b>IMbnDeviceServicesContext</b> objects are provided by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesmanager-getdeviceservicescontext">GetDeviceServicesContext</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesmanager">IMbnDeviceServicesManager</a> interface.



