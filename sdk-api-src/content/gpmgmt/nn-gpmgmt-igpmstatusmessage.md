---
UID: NN:gpmgmt.IGPMStatusMessage
title: IGPMStatusMessage (gpmgmt.h)
description: The IGPMStatusMessage interface contains property methods that retrieve various properties of status messages related to GPO operations.
old-location: gpmc\igpmstatusmessage.htm
tech.root: gpmc
ms.assetid: 8570d40c-25c2-405c-b52a-dae6c0eb50e0
ms.date: 12/05/2018
ms.keywords: GPMStatusMessage, IGPMStatusMessage, IGPMStatusMessage interface [GPMC], IGPMStatusMessage interface [GPMC],described, _win32_igpmstatusmessage, gpmc.igpmstatusmessage, gpmgmt/IGPMStatusMessage
f1_keywords:
- gpmgmt/IGPMStatusMessage
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMStatusMessage interface


## -description


The 
<b>IGPMStatusMessage</b> interface contains property methods that retrieve various properties of status messages related to GPO operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStatusMessage</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStatusMessage</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstatusmessage-errorcode">ErrorCode</a>
</td>
<td align="left" width="63%">
Returns the actual error that occurred during the GPMC operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstatusmessage-operationcode">OperationCode</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstatusmessage-property-methods">ExtensionName</a>


</td>
<td align="left" width="63%">
Name of the extension that was being processed when the message was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstatusmessage-property-methods">Message</a>


</td>
<td align="left" width="63%">
Message, in human-readable format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstatusmessage-property-methods">ObjectPath</a>


</td>
<td align="left" width="63%">
Path of the object to which the message applies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstatusmessage-property-methods">SettingsName</a>


</td>
<td align="left" width="63%">
Name of the policy setting that was being processed when the message was generated.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
 

 

