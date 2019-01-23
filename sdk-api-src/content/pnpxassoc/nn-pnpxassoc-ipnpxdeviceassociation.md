---
UID: NN:pnpxassoc.IPNPXDeviceAssociation
title: IPNPXDeviceAssociation
author: windows-sdk-content
description: Defines methods to manage the association database entries for PnP-X devices. These methods send notifications when the corresponding PnP devnode changes.
old-location: ncd\ipnpxdeviceassociation.htm
tech.root: FunDisc
ms.assetid: 52669dec-2fd7-4f3e-b322-e93d9da5984d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPNPXDeviceAssociation, IPNPXDeviceAssociation interface, IPNPXDeviceAssociation interface,described, ncd.ipnpxdeviceassociation, pnpxassoc/IPNPXDeviceAssociation
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - pnpxassoc.h
api_name:
 - IPNPXDeviceAssociation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPNPXDeviceAssociation interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Defines methods to manage the association database entries for  PnP-X devices. These methods send notifications when the corresponding PnP devnode changes. An application calls <b>IPNPXDeviceAssociation</b> methods when the application programmatically manages PnP-X device association, either through a custom user interface or through some other method. Usually, the <b>Network Explorer</b> is used to manage PnP-X device association.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPNPXDeviceAssociation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPNPXDeviceAssociation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPNPXDeviceAssociation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2024c2b8-ef47-4352-80ea-c68b22f38d4c">IPNPXDeviceAssociation::Associate</a>
</td>
<td align="left" width="63%">
Marks an association database entry as associated and sends an appropriate notification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/208da586-6bb3-4365-90ba-9fd615a371eb">IPNPXDeviceAssociation::Delete</a>
</td>
<td align="left" width="63%">
Removes an entry from the association database and sends an appropriate notification. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb420967-c79c-4edd-a432-b982219c0746">IPNPXDeviceAssociation::Unassociate</a>
</td>
<td align="left" width="63%">
Marks an association database entry as unassociated and sends an appropriate notification.   

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">QueryService</a> on a function instance returned by a Function Discovery query. The following pseudocode shows the parameters to use for the  <b>QueryService</b> call.

<pre class="syntax" xml:space="preserve"><code>QueryService( SID_PNPXAssociation, __uuidof( IPNPXDeviceAssociation ) )</code></pre>
The <b>IPNPXDeviceAssociation</b> methods modify the association database entry for the function instance upon which <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">QueryService</a>  was called.

Not all function instances can be associated using the <b>IPNPXDeviceAssociation</b> methods. The function instance must have its  PKEY_PNPX_GlobalIdentity key populated with the UUID supplied by the Function Discovery provider used to discover the device. For more information about property keys, see <a href="https://msdn.microsoft.com/d297705b-d825-4aa5-8269-ef44bc5875d7">PnP-X Provider PKEYs</a>.




## -see-also




<a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a>
 

 

