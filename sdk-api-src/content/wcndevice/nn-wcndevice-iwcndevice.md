---
UID: NN:wcndevice.IWCNDevice
title: IWCNDevice (wcndevice.h)
author: windows-sdk-content
description: Use this interface to configure the device and initiate the session.
old-location: wcn\iwcndevice.htm
tech.root: wcn
ms.assetid: a092406d-7af4-436d-9755-5a9b87aa6ca9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWCNDevice, IWCNDevice interface [Windows Connect Now], IWCNDevice interface [Windows Connect Now],described, wcn.iwcndevice, wcndevice/IWCNDevice
ms.topic: interface
f1_keywords: 
 - "wcndevice/IWCNDevice"
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - WcnDevice.h
api_name:
 - IWCNDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWCNDevice interface


## -description


Use this interface to configure the device and initiate the session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCNDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCNDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWCNDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">Connect</a>
</td>
<td align="left" width="63%">
Initiates the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getattribute">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute  from the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getintegerattribute">GetIntegerAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute  from the device as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getnetworkprofile">GetNetworkProfile</a>
</td>
<td align="left" width="63%">
Gets a network profile from the device.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getstringattribute">GetStringAttribute</a>
</td>
<td align="left" width="63%">
Gets a cached attribute from the device as a string.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-getvendorextension">GetVendorExtension</a>
</td>
<td align="left" width="63%">
Gets a cached vendor extension from the device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setnetworkprofile">SetNetworkProfile</a>
</td>
<td align="left" width="63%">
Queues an XML WLAN profile to be provisioned to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">SetPassword</a>
</td>
<td align="left" width="63%">
Configures the authentication method value, and if required, a password used for the pending session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setvendorextension">SetVendorExtension</a>
</td>
<td align="left" width="63%">
Queues a vendor extension for use in the pending session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Removes any callback previously set via <a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>
 

 

