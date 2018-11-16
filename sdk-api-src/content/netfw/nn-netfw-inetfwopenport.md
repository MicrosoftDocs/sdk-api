---
UID: NN:netfw.INetFwOpenPort
title: INetFwOpenPort
author: windows-sdk-content
description: The INetFwOpenPort interface provides access to the properties of a port that has been opened in the firewall.
old-location: ics\inetfwopenport.htm
tech.root: ICS
ms.assetid: 1a9fd676-b1c0-4be5-9571-d14ac5980af5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: INetFwOpenPort, INetFwOpenPort interface [ICS/ICF], INetFwOpenPort interface [ICS/ICF],described, ics.inetfwopenport, netfw/INetFwOpenPort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwOpenPort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwOpenPort interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwOpenPort</b> interface provides access to the properties of a port that has been opened in the firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPort</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwOpenPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwOpenPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7260b9f2-2cbe-4b71-8c99-1d1c30870ae1">get_BuiltIn</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the BuiltIn property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4fc7a4f-abc5-486a-89c8-dfea17770f3c">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb5dfb78-fc0d-4dca-850a-683046b4e2a3">get_IpVersion</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f81abb86-095c-4459-af71-a0c10f7b1acd">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e179f11-76c3-4403-9b42-2faad56629ed">get_Port</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/775c3d29-89c7-4768-9476-2e56555fd82b">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the  RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">get_Scope</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4fc7a4f-abc5-486a-89c8-dfea17770f3c">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb5dfb78-fc0d-4dca-850a-683046b4e2a3">put_IpVersion</a>
</td>
<td align="left" width="63%">
Sets the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f81abb86-095c-4459-af71-a0c10f7b1acd">put_Name</a>
</td>
<td align="left" width="63%">
Sets the contents of the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e179f11-76c3-4403-9b42-2faad56629ed">put_Port</a>
</td>
<td align="left" width="63%">
Sets the contents of the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/775c3d29-89c7-4768-9476-2e56555fd82b">put_Protocol</a>
</td>
<td align="left" width="63%">
Sets the contents of the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Modifies the contents of the  RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">put_Scope</a>
</td>
<td align="left" width="63%">
Modifies the contents of the Scope property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPort</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7260b9f2-2cbe-4b71-8c99-1d1c30870ae1">BuiltIn</a>


</td>
<td align="left" width="63%">
Accesses the contents of the BuiltIn property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f4fc7a4f-abc5-486a-89c8-dfea17770f3c">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fb5dfb78-fc0d-4dca-850a-683046b4e2a3">IpVersion</a>


</td>
<td align="left" width="63%">
Accesses the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f81abb86-095c-4459-af71-a0c10f7b1acd">Name</a>


</td>
<td align="left" width="63%">
Accesses the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6e179f11-76c3-4403-9b42-2faad56629ed">Port</a>


</td>
<td align="left" width="63%">
Accesses the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/775c3d29-89c7-4768-9476-2e56555fd82b">Protocol</a>


</td>
<td align="left" width="63%">
Accesses the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">Scope</a>


</td>
<td align="left" width="63%">
Accesses the  Scope property.

</td>
</tr>
</table> 


## -remarks



Ports  with their <b>BuiltIn</b> property set to true (<b>VARIANT_TRUE</b>) are system specified and cannot be removed.

When creating new ports, this interface is supported by the
<b>HNetCfg.FWOpenPort</b> COM object. 

For reading or modifying existing ports,
instances of this interface are retrieved through the <a href="https://msdn.microsoft.com/a3a6e5c1-5818-419c-8df4-966b2fbcd8c0">INetFwOpenPorts</a>collection. 

All configuration changes take effect immediately.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/a3a6e5c1-5818-419c-8df4-966b2fbcd8c0">INetFwOpenPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

