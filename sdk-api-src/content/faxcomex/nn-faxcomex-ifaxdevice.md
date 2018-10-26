---
UID: NN:faxcomex.IFaxDevice
title: IFaxDevice
author: windows-sdk-content
description: The IFaxDevice interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device.
old-location: fax\_mfax_faxdevice_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5nad_cpp.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxDevice, IFaxDevice interface [Fax Service], IFaxDevice interface [Fax Service],described, _mfax_faxdevice_cpp, fax._mfax_faxdevice_cpp, faxcomex/IFaxDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevice interface


## -description


The <b>IFaxDevice</b> interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device. The object also includes methods to retrieve and set extension configuration properties stored at the device level. The object defined by the <b>IFaxDevice</b> interface represents a single device associated with a fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686924(v=VS.85).aspx">AnswerCall</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686924(v=VS.85).aspx">IFaxDevice::AnswerCall</a> method causes the fax device to answer an incoming call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687465(v=VS.85).aspx">GetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687465(v=VS.85).aspx">IFaxDevice::get_GetExtensionProperty</a> method retrieves an extension configuration property stored at the device level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686727(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686727(v=VS.85).aspx">IFaxDevice::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object information from the fax server. When the <b>IFaxDevice::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms686131(v=VS.85).aspx">IFaxDevice::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686131(v=VS.85).aspx">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686131(v=VS.85).aspx">IFaxDevice::Save</a> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object's data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686482(v=VS.85).aspx">SetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686482(v=VS.85).aspx">IFaxDevice::SetExtensionProperty</a> method stores an extension configuration property at the device level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685094(v=VS.85).aspx">UseRoutingMethod</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685094(v=VS.85).aspx">IFaxDevice::UseRoutingMethod</a> method adds an inbound fax routing method to or removes a fax routing method (<a href="https://msdn.microsoft.com/en-us/library/ms687469(v=VS.85).aspx">FaxInboundRoutingMethod</a>) from the list of routing methods associated with the fax device.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevice</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686490(v=VS.85).aspx">CSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686490(v=VS.85).aspx">IFaxDevice::get_CSID</a> property is a null-terminated string that contains the CSID for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687095(v=VS.85).aspx">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687095(v=VS.85).aspx">IFaxDevice::get_Description</a> property is a null-terminated string that contains a user-friendly description for the fax device. This string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686186(v=VS.85).aspx">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686186(v=VS.85).aspx">IFaxDevice::get_DeviceName</a> property is a null-terminated string that contains the name of the fax device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684582(v=VS.85).aspx">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The Id <a href="https://msdn.microsoft.com/en-us/library/ms684582(v=VS.85).aspx">IFaxDevice::get_Id</a> is a numeric value that uniquely identifies a fax device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685062(v=VS.85).aspx">PoweredOff</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms685062(v=VS.85).aspx">IFaxDevice::get_PoweredOff</a> property is a Boolean value that indicates whether the fax device is currently available for sending and receiving faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684864(v=VS.85).aspx">ProviderUniqueName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684864(v=VS.85).aspx">IFaxDevice::get_ProviderUniqueName</a> property is a null-terminated string that contains the unique name for the FSP associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684559(v=VS.85).aspx">ReceiveMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684558(v=VS.85).aspx">ReceiveMode</a> property is a value from the <a href="https://msdn.microsoft.com/en-us/library/ms689547(v=VS.85).aspx">FAX_DEVICE_RECEIVE_MODE_ENUM</a> enumeration that defines the way a device answers an incoming call. The value assigned to this property indicates whether the device does not answer the call, the device can answer the call manually, or the device answers the call automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686513(v=VS.85).aspx">ReceivingNow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686513(v=VS.85).aspx">IFaxDevice::get_ReceivingNow</a> property is a Boolean value that indicates whether the fax device is receiving a fax at the moment the property is retrieved (the status could change immediately thereafter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms687114(v=VS.85).aspx">RingingNow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms687114(v=VS.85).aspx">IFaxDevice::get_RingingNow</a> property is a Boolean value that indicates whether the fax device is ringing at the moment the property is retrieved (the status could change immediately thereafter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684551(v=VS.85).aspx">RingsBeforeAnswer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684551(v=VS.85).aspx">IFaxDevice::get_RingsBeforeAnswer</a> property is a number that specifies the number of rings that occur before the fax device answers an incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686508(v=VS.85).aspx">SendEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686508(v=VS.85).aspx">IFaxDevice::get_SendEnabled</a> property is a Boolean value that indicates whether the fax device is enabled for sending faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686017(v=VS.85).aspx">SendingNow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686017(v=VS.85).aspx">IFaxDevice::get_SendingNow</a> property is a Boolean value that indicates whether the fax device is sending a fax at the moment the property is retrieved (the status could change immediately thereafter). 

            

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/en-us/library/ms686727(v=VS.85).aspx">IFaxDevice::Refresh</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms684811(v=VS.85).aspx">TSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms684811(v=VS.85).aspx">IFaxDevice::get_TSID</a> property is a null-terminated string that contains the TSID for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686520(v=VS.85).aspx">UsedRoutingMethods</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms686520(v=VS.85).aspx">IFaxDevice::get_UsedRoutingMethods</a> property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (<a href="https://msdn.microsoft.com/en-us/library/ms687469(v=VS.85).aspx">FaxInboundRoutingMethod</a>).

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDevice</b> is provided as the <a href="https://msdn.microsoft.com/en-us/library/ms686192(v=VS.85).aspx">FaxDevice</a> object.



