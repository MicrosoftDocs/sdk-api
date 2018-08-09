---
UID: NF:pnpxassoc.IPNPXDeviceAssociation.Associate
title: IPNPXDeviceAssociation::Associate
author: windows-sdk-content
description: Marks an association database entry as associated and sends an appropriate notification.
old-location: ncd\ipnpxdeviceassociation_associate.htm
old-project: fundisc
ms.assetid: 2024c2b8-ef47-4352-80ea-c68b22f38d4c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Associate, Associate method, Associate method,IPNPXDeviceAssociation interface, IPNPXDeviceAssociation interface,Associate method, IPNPXDeviceAssociation.Associate, IPNPXDeviceAssociation::Associate, ncd.ipnpxdeviceassociation_associate, pnpxassoc/IPNPXDeviceAssociation::Associate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - pnpxassoc.h
api_name:
 - IPNPXDeviceAssociation.Associate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPNPXDeviceAssociation::Associate


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Marks an association database entry as associated and sends an appropriate notification.  If there is no association database entry for the function instance, one is created; otherwise the existing entry is updated. Any notification sent reflects the online presence of the device, as reported by the Plug and Play (PnP) component.


## -parameters




### -param pszSubCategory [in, optional]

The subcategory of the association database in which the entry is stored.  This parameter can be <b>NULL</b>.


### -param pIFunctionDiscoveryNotification [in]

An <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> object that is registered for notifications with Function Discovery. 


## -returns



This method can return one of these values.

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



This method modifies the association database entry corresponding to the function instance from which the <a href="https://msdn.microsoft.com/52669dec-2fd7-4f3e-b322-e93d9da5984d">IPNPXDeviceAssociation</a> interface was obtained. 

Once a device is associated, the PnP-X Service IP Bus Enumerator (IPBusEnum) sends a request to the PnP component  to create the device <a href="function_discovery_glossary.htm">devnode</a>. Once the devnode has been created, the appropriate notification is sent. The following logic is used to determine the callback method used for notification:

<ul>
<li>If a PnP notification is received after the device is associated, then the <a href="https://msdn.microsoft.com/ab4d0fc6-de3f-49cf-b53c-573222a8bc89">IFunctionDiscoveryNotification::OnUpdate</a> method is called  with the <i>enumQueryUpdateAction</i> parameter set to  <b>QUA_ADD</b>. </li>
<li>If no PnP notification is received after the device is associated, and there are no pending PnP events, then the <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">IFunctionDiscoveryNotification::OnError</a> method is called. </li>
<li>Finally, if no PnP notification is received after the device is associated, and there are pending PnP events, then no callback method is called.</li>
</ul>
The <b>Found New Hardware</b> wizard appears if user intervention is required to install a device driver after association.




## -see-also




<a href="https://msdn.microsoft.com/74d2ed38-9362-4664-9384-e773e4ec76f3">IPNPXAssociation::Associate</a>



<a href="https://msdn.microsoft.com/52669dec-2fd7-4f3e-b322-e93d9da5984d">IPNPXDeviceAssociation</a>
 

 

