---
UID: NF:pnpxassoc.IPNPXDeviceAssociation.Delete
title: IPNPXDeviceAssociation::Delete (pnpxassoc.h)
description: Removes an entry from the association database and sends an appropriate notification.
helpviewer_keywords: ["Delete","Delete method","Delete method","IPNPXDeviceAssociation interface","IPNPXDeviceAssociation interface","Delete method","IPNPXDeviceAssociation.Delete","IPNPXDeviceAssociation::Delete","ncd.ipnpxdeviceassociation_delete","pnpxassoc/IPNPXDeviceAssociation::Delete"]
old-location: ncd\ipnpxdeviceassociation_delete.htm
tech.root: ncd
ms.assetid: 208da586-6bb3-4365-90ba-9fd615a371eb
ms.date: 12/05/2018
ms.keywords: Delete, Delete method, Delete method,IPNPXDeviceAssociation interface, IPNPXDeviceAssociation interface,Delete method, IPNPXDeviceAssociation.Delete, IPNPXDeviceAssociation::Delete, ncd.ipnpxdeviceassociation_delete, pnpxassoc/IPNPXDeviceAssociation::Delete
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
 - IPNPXDeviceAssociation::Delete
 - pnpxassoc/IPNPXDeviceAssociation::Delete
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
 - IPNPXDeviceAssociation.Delete
---

# IPNPXDeviceAssociation::Delete


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes an entry from the association database and sends an appropriate notification.

## -parameters

### -param pszSubcategory [in, optional]

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
<li>If a PnP notification is received after the device is deleted, then the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">IFunctionDiscoveryNotification::OnUpdate</a> method is called  with the <i>enumQueryUpdateAction</i> parameter set to  <b>QUA_REMOVE</b>. </li>
<li>If no PnP notification is received after the device is deleted, and there are no pending PnP events, then the <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">IFunctionDiscoveryNotification::OnError</a> method is called. </li>
<li>Finally, if no PnP notification is received after the device is deleted, and there are pending PnP events, then no callback method is called.</li>
</ul>
To mark a device as unavailable for use without deleting the association database entry, call <a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-unassociate">IPNPXDeviceAssociation::Unassociate</a>.

## -see-also

<a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxassociation-delete">IPNPXAssociation::Delete</a>



<a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxdeviceassociation">IPNPXDeviceAssociation</a>