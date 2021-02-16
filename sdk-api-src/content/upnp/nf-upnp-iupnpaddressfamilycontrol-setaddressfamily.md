---
UID: NF:upnp.IUPnPAddressFamilyControl.SetAddressFamily
title: IUPnPAddressFamilyControl::SetAddressFamily (upnp.h)
description: The SetAddressFamily method sets the address family flag of the Device Finder object, which uses this flag to filter the devices found.
helpviewer_keywords: ["IUPnPAddressFamilyControl interface [UPnP APIs]","SetAddressFamily method","IUPnPAddressFamilyControl.SetAddressFamily","IUPnPAddressFamilyControl::SetAddressFamily","SetAddressFamily","SetAddressFamily method [UPnP APIs]","SetAddressFamily method [UPnP APIs]","IUPnPAddressFamilyControl interface","UPNP_ADDRESSFAMILY_BOTH","UPNP_ADDRESSFAMILY_IPv4","UPNP_ADDRESSFAMILY_IPv6","upnp.iupnpaddressfamilycontrol_setaddressfamily","upnp/IUPnPAddressFamilyControl::SetAddressFamily"]
old-location: upnp\iupnpaddressfamilycontrol_setaddressfamily.htm
tech.root: upnp
ms.assetid: 2b3e5dae-68c0-431b-bef0-fa2bb5f53bdc
ms.date: 12/05/2018
ms.keywords: IUPnPAddressFamilyControl interface [UPnP APIs],SetAddressFamily method, IUPnPAddressFamilyControl.SetAddressFamily, IUPnPAddressFamilyControl::SetAddressFamily, SetAddressFamily, SetAddressFamily method [UPnP APIs], SetAddressFamily method [UPnP APIs],IUPnPAddressFamilyControl interface, UPNP_ADDRESSFAMILY_BOTH, UPNP_ADDRESSFAMILY_IPv4, UPNP_ADDRESSFAMILY_IPv6, upnp.iupnpaddressfamilycontrol_setaddressfamily, upnp/IUPnPAddressFamilyControl::SetAddressFamily
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPAddressFamilyControl::SetAddressFamily
 - upnp/IUPnPAddressFamilyControl::SetAddressFamily
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPAddressFamilyControl.SetAddressFamily
---

# IUPnPAddressFamilyControl::SetAddressFamily


## -description

The <b>SetAddressFamily</b> method sets the address family flag of the Device Finder object, which uses this flag to filter the devices found.

The application sets the address family flag before starting a search. The application will be notified only about devices that have IP addresses that are of the specified address family.

## -parameters

### -param dwFlags [in]

Integer (4-byte value) that specifies the address family to be used by the Device Finder object to filter the devices found.

The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv4"></a><a id="upnp_addressfamily_ipv4"></a><a id="UPNP_ADDRESSFAMILY_IPV4"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv4</b></dt>
</dl>
</td>
<td width="60%">
IPv4 (IP version 4)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv6"></a><a id="upnp_addressfamily_ipv6"></a><a id="UPNP_ADDRESSFAMILY_IPV6"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv6</b></dt>
</dl>
</td>
<td width="60%">
IPv6 (IP version 6)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_BOTH"></a><a id="upnp_addressfamily_both"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_BOTH</b></dt>
</dl>
</td>
<td width="60%">
IPv4 and IPv6

</td>
</tr>
</table>

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

<h3><a id="Setting__the_Flag"></a><a id="setting__the_flag"></a><a id="SETTING__THE_FLAG"></a>Setting  the Flag</h3>

The address family flag must be set at the appropriate time in order to affect the search:

<ul>
<li>For an asynchronous search, set the address family flag prior to calling the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a> method.</li>
<li>For a synchronous search, set the address family flag prior to calling either the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbyudn">IUPnPDeviceFinder::FindByUDN</a> or <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbytype">IUPnPDeviceFinder::FindByType</a> method.</li>
</ul>


<h3><a id="Filtering_the_Devices_Found"></a><a id="filtering_the_devices_found"></a><a id="FILTERING_THE_DEVICES_FOUND"></a>Filtering the Devices Found</h3>

Scenario 1: a control point application sets the address family flag to UPNP_ADDRESSFAMILY_IPV4, and then starts a search:

<ul>
<li>If the Device Finder  discovers a device that has an IPv6 address, Device Finder will not notify the application of the device. If the same device later acquires an IPv4 address, Device Finder will notify the application of the device and provide the IPv4 address.</li>
<li>If the Device Finder discovers a device that has an IPv4 address, Device Finder will notify the application of the device and provide the IPv4 address. If the same device later acquires an IPv6 address, Device Finder will not notify the application of the device's additional address.</li>
<li>If Device Finder  discovers a device that has both IPv4 and IPv6 addresses, it will notify the application of the device, but it will provide only the IPv4 address.</li>
<li>If a device that is known to the application announces an address change, Device Finder will notify the application of the change only when the new address is an IPv4 address.</li>
<li>If a device that is known to the application has both IPv4 and IPv6 addresses and Device Finder receives a bye-bye message from the device's IPv6 address, Device Finder will notify the application even though the application is aware of only the IPv4 address. In other words, if a device that is known to the application leaves the network, Device Finder will notify the application regardless of the device's address.</li>
</ul>



Scenario 2: an application sets the address family flag to UPNP_ADDRESSFAMILY_IPV6, and then starts a search:

<ul>
<li>A similar set of rules apply as described in Scenario 1, but for the opposite address family.</li>
</ul>



Scenario 3: an application sets the address family flag to UPNP_ADDRESSFAMILY_BOTH, and then starts a search:

<ul>
<li>If the Device Finder discovers a device that has either an IPv4 address or an IPv6 address, Device Finder will notify the application of the device and provide the address. If the same device later acquires an address that is of a different address family, Device Finder will not notify the application of the device's additional address.</li>
<li>If Device Finder discovers a device that has both IPv4 and IPv6 addresses, it will notify the application of the device, but it will provide only one of the  addresses, chosen randomly.</li>
<li>If a device that is known to the application announces an address change, Device Finder will notify the application of the change.</li>
<li>If a device that is known to the application leaves the network, Device Finder will notify the application.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpaddressfamilycontrol-getaddressfamily">GetAddressFamily</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpaddressfamilycontrol">IUPnPAddressFamilyControl</a>