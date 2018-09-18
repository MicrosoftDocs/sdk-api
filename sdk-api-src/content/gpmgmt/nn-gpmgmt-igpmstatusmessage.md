---
UID: NN:gpmgmt.IGPMStatusMessage
title: IGPMStatusMessage
author: windows-sdk-content
description: The IGPMStatusMessage interface contains property methods that retrieve various properties of status messages related to GPO operations.
old-location: gpmc\igpmstatusmessage.htm
tech.root: GPMC
ms.assetid: 8570d40c-25c2-405c-b52a-dae6c0eb50e0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMStatusMessage, IGPMStatusMessage, IGPMStatusMessage interface [GPMC], IGPMStatusMessage interface [GPMC],described, _win32_igpmstatusmessage, gpmc.igpmstatusmessage, gpmgmt/IGPMStatusMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMStatusMessage
 - GPMStatusMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStatusMessage interface


## -description


The 
<b>IGPMStatusMessage</b> interface contains property methods that retrieve various properties of status messages related to GPO operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMessage</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMStatusMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStatusMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a50523-1acb-4b58-b867-ec19b0cf960a">ErrorCode</a>
</td>
<td align="left" width="63%">
Returns the actual error that occurred during the GPMC operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f99dc90a-fabe-40fb-8289-36501a68b11d">OperationCode</a>
</td>
<td align="left" width="63%">
Returns a code related to the GPMC operation indicating a specific failure or warning for the operation.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMessage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d736e30-760d-43fa-ab5d-d05dc679bfbb">ExtensionName</a>


</td>
<td align="left" width="63%">
Name of the extension that was being processed when the message was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d736e30-760d-43fa-ab5d-d05dc679bfbb">Message</a>


</td>
<td align="left" width="63%">
Message, in human-readable format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d736e30-760d-43fa-ab5d-d05dc679bfbb">ObjectPath</a>


</td>
<td align="left" width="63%">
Path of the object to which the message applies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d736e30-760d-43fa-ab5d-d05dc679bfbb">SettingsName</a>


</td>
<td align="left" width="63%">
Name of the policy setting that was being processed when the message was generated.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/774dd1b0-e5ea-4fef-b3bc-743870793db5">IGPMStatusMsgCollection</a>
 

 

