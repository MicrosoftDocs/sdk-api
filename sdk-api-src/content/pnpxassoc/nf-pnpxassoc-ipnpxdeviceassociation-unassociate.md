---
UID: NF:pnpxassoc.IPNPXDeviceAssociation.Unassociate
title: IPNPXDeviceAssociation::Unassociate (pnpxassoc.h)
description: Marks an association database entry as unassociated and sends an appropriate notification.
helpviewer_keywords: ["IPNPXDeviceAssociation interface","Unassociate method","IPNPXDeviceAssociation.Unassociate","IPNPXDeviceAssociation::Unassociate","Unassociate","Unassociate method","Unassociate method","IPNPXDeviceAssociation interface","ncd.ipnpxdeviceassociation_unassociate","pnpxassoc/IPNPXDeviceAssociation::Unassociate"]
old-location: ncd\ipnpxdeviceassociation_unassociate.htm
tech.root: ncd
ms.assetid: fb420967-c79c-4edd-a432-b982219c0746
ms.date: 12/05/2018
ms.keywords: IPNPXDeviceAssociation interface,Unassociate method, IPNPXDeviceAssociation.Unassociate, IPNPXDeviceAssociation::Unassociate, Unassociate, Unassociate method, Unassociate method,IPNPXDeviceAssociation interface, ncd.ipnpxdeviceassociation_unassociate, pnpxassoc/IPNPXDeviceAssociation::Unassociate
req.header: pnpxassoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPNPXDeviceAssociation::Unassociate
 - pnpxassoc/IPNPXDeviceAssociation::Unassociate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - pnpxassoc.h
api_name:
 - IPNPXDeviceAssociation.Unassociate
---

# IPNPXDeviceAssociation::Unassociate


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Marks an association database entry as unassociated and sends an appropriate notification.

## -parameters

### -param pszSubCategory [in, optional]

The subcategory of the association database in which the entry is stored.  This parameter can be <b>NULL</b>.

### -param pIFunctionDiscoveryNotification [in]

An <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> object that is registered for notifications with Function Discovery.

## -returns

Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>

## -remarks

This method modifies the association database entry corresponding to the function instance from which the <a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxdeviceassociation">IPNPXDeviceAssociation</a> interface was obtained. 

The following logic is used to determine the callback method used for notification:

<ul>
<li>If a PnP notification is received after the device is unassociated, then the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">IFunctionDiscoveryNotification::OnUpdate</a> method is called  with the <i>enumQueryUpdateAction</i> parameter set to  <b>QUA_REMOVE</b>. </li>
<li>If no PnP notification is received after the device is unassociated, and there are no pending PnP events, then the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">IFunctionDiscoveryNotification::OnError</a> method is called. </li>
<li>Finally, if no PnP notification is received after the device is unassociated, and there are pending PnP events, then no callback method is called.</li>
</ul>
This method does not remove the entry from the association database. To remove an entry from the association database, call <a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxassociation-delete">IPNPXAssociation::Delete</a>.

## -see-also

<a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxassociation-unassociate">IPNPXAssociation::Unassociate</a>



<a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxdeviceassociation">IPNPXDeviceAssociation</a>