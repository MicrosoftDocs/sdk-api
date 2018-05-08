---
UID: NN:faxcomex.IFaxDevice
title: IFaxDevice
author: windows-driver-content
description: The IFaxDevice interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device.
old-location: fax\_mfax_faxdevice_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5nad_cpp.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFaxDevice, IFaxDevice interface [Fax Service], IFaxDevice interface [Fax Service],described, _mfax_faxdevice_cpp, fax._mfax_faxdevice_cpp, faxcomex/IFaxDevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDevice interface


## -description


The <b>IFaxDevice</b> interface defines a configuration object used by a fax client application to retrieve and set fax device information, and to add and remove fax routing methods associated with a fax device. The object also includes methods to retrieve and set extension configuration properties stored at the device level. The object defined by the <b>IFaxDevice</b> interface represents a single device associated with a fax server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxDevice</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFaxDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5cbc143f-549d-4487-8416-158784d516bb">AnswerCall</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5cbc143f-549d-4487-8416-158784d516bb">IFaxDevice::AnswerCall</a> method causes the fax device to answer an incoming call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b0c96ca-072b-4f4e-bfca-4bf8aab5fc5e">GetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5b0c96ca-072b-4f4e-bfca-4bf8aab5fc5e">IFaxDevice::get_GetExtensionProperty</a> method retrieves an extension configuration property stored at the device level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">Refresh</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">IFaxDevice::Refresh</a> method refreshes <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object information from the fax server. When the <b>IFaxDevice::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/16183ae9-0bfc-4717-867b-88dd3eb7c9ff">IFaxDevice::Save</a> method call are lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/16183ae9-0bfc-4717-867b-88dd3eb7c9ff">IFaxDevice::Save</a> method saves the <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object's data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/640fe0ba-099b-447d-bbca-1219c7644e86">SetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/640fe0ba-099b-447d-bbca-1219c7644e86">IFaxDevice::SetExtensionProperty</a> method stores an extension configuration property at the device level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcfe525b-6478-4202-839c-8ba984965bdb">UseRoutingMethod</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fcfe525b-6478-4202-839c-8ba984965bdb">IFaxDevice::UseRoutingMethod</a> method adds an inbound fax routing method to or removes a fax routing method (<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>) from the list of routing methods associated with the fax device.

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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn922691">CSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/75df5662-3686-44d3-b210-2eb5a7180ba2">IFaxDevice::get_CSID</a> property is a null-terminated string that contains the CSID for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/79e538fc-4df5-4b7e-938e-ae9ce78a50a9">IFaxDevice::get_Description</a> property is a null-terminated string that contains a user-friendly description for the fax device. This string is suitable for display to users.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt188594">DeviceName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e21635b8-89a7-401b-9e0a-fa99fe35f3e2">IFaxDevice::get_DeviceName</a> property is a null-terminated string that contains the name of the fax device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The Id <a href="https://msdn.microsoft.com/84e54535-4b40-4572-b8e1-3ab5095dbd6a">IFaxDevice::get_Id</a> is a numeric value that uniquely identifies a fax device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d4128187-e5be-456d-acb9-38d8ce67ec08">PoweredOff</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d4128187-e5be-456d-acb9-38d8ce67ec08">IFaxDevice::get_PoweredOff</a> property is a Boolean value that indicates whether the fax device is currently available for sending and receiving faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4082b2ce-33a3-4bec-877a-a246f1f0613e">ProviderUniqueName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4082b2ce-33a3-4bec-877a-a246f1f0613e">IFaxDevice::get_ProviderUniqueName</a> property is a null-terminated string that contains the unique name for the FSP associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f0a988d-76a1-49e1-b59f-4ecebb67c944">ReceiveMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d65397eb-2ede-4320-82ea-8fc48aa3f2b0">ReceiveMode</a> property is a value from the <a href="https://msdn.microsoft.com/0fb87bfd-61b0-4130-86fd-0e6579bc55ea">FAX_DEVICE_RECEIVE_MODE_ENUM</a> enumeration that defines the way a device answers an incoming call. The value assigned to this property indicates whether the device does not answer the call, the device can answer the call manually, or the device answers the call automatically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/455ce61c-8a0e-4877-a279-a4a8888c20b8">ReceivingNow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/455ce61c-8a0e-4877-a279-a4a8888c20b8">IFaxDevice::get_ReceivingNow</a> property is a Boolean value that indicates whether the fax device is receiving a fax at the moment the property is retrieved (the status could change immediately thereafter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d3f04619-e1fa-4965-b76c-eb26163ba336">RingingNow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d3f04619-e1fa-4965-b76c-eb26163ba336">IFaxDevice::get_RingingNow</a> property is a Boolean value that indicates whether the fax device is ringing at the moment the property is retrieved (the status could change immediately thereafter).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f025eaa-9506-458b-85c9-3cc11cab6440">RingsBeforeAnswer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3f025eaa-9506-458b-85c9-3cc11cab6440">IFaxDevice::get_RingsBeforeAnswer</a> property is a number that specifies the number of rings that occur before the fax device answers an incoming fax call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bfa3cafa-695a-42b5-a088-ad5e8dac1f20">SendEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bfa3cafa-695a-42b5-a088-ad5e8dac1f20">IFaxDevice::get_SendEnabled</a> property is a Boolean value that indicates whether the fax device is enabled for sending faxes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9a932c65-c18a-4964-b72a-fe7b989d97ba">SendingNow</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9a932c65-c18a-4964-b72a-fe7b989d97ba">IFaxDevice::get_SendingNow</a> property is a Boolean value that indicates whether the fax device is sending a fax at the moment the property is retrieved (the status could change immediately thereafter). 

            

<div class="alert"><b>Note</b>  The value of this property is set at the time that the <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object is created and is refreshed when you call the <a href="https://msdn.microsoft.com/9517a067-d29b-4362-a3ca-0658498aba5e">IFaxDevice::Refresh</a> method.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997387">TSID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/773960cf-22d6-4b0f-aaf5-704458463648">IFaxDevice::get_TSID</a> property is a null-terminated string that contains the TSID for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9321db17-073c-4c99-9f3f-4bbc1703f71e">UsedRoutingMethods</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9321db17-073c-4c99-9f3f-4bbc1703f71e">IFaxDevice::get_UsedRoutingMethods</a> property is an array of strings that contains the GUIDs associated with the routing methods that the device uses, where each GUID represents an inbound routing method (<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>).

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxDevice</b> is provided as the <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object.



