---
UID: NN:pnpxassoc.IPNPXAssociation
title: IPNPXAssociation
author: windows-sdk-content
description: Defines methods to manage the association database entries for PnP-X devices.
old-location: ncd\ipnpxassociation.htm
old-project: FunDisc
ms.assetid: 03c1c4cb-fffb-4b4a-963a-200670062f4a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IPNPXAssociation, IPNPXAssociation interface, IPNPXAssociation interface,described, ncd.ipnpxassociation, pnpxassoc/IPNPXAssociation
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	pnpxassoc.h
api_name:
-	IPNPXAssociation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPNPXAssociation interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Defines methods to manage the association database entries for  PnP-X devices. . These methods send notifications when the corresponding PnP devnode changes.  An application calls <b>IPNPXAssociation</b> methods when the application programmatically manages PnP-X device association, either through a custom user interface or through some other method. Usually, the <b>Network Explorer</b> is used to manage PnP-X device association.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPNPXAssociation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPNPXAssociation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPNPXAssociation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d2ed38-9362-4664-9384-e773e4ec76f3">IPNPXAssociation::Associate</a>
</td>
<td align="left" width="63%">
Marks an association database entry as associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc00c135-140d-4e05-9180-779917d88688">IPNPXAssociation::Delete</a>
</td>
<td align="left" width="63%">
Removes an entry from the association database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92f0cc10-03a0-498f-acd1-4b03302aa33b">IPNPXAssociation::Unassociate</a>
</td>
<td align="left" width="63%">
Marks an association database entry as unassociated. 

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">QueryService</a> on a function instance returned by a Function Discovery query. The following pseudocode shows the parameters to use for the  <b>QueryService</b> call.

<pre class="syntax" xml:space="preserve"><code>QueryService( SID_PNPXAssociation, __uuidof( IPNPXAssociation ) )</code></pre>
The <b>IPNPXAssociation</b> methods modify the association database entry for the function instance upon which <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">QueryService</a>  was called.

Not all function instances can be associated using the <b>IPNPXAssociation</b> methods. The function instance must have its  PKEY_PNPX_GlobalIdentity key populated with the UUID supplied by the Function Discovery provider used to discover the device. For more information about property keys, see <a href="https://msdn.microsoft.com/d297705b-d825-4aa5-8269-ef44bc5875d7">PnP-X Provider PKEYs</a>.




## -see-also




<a href="https://msdn.microsoft.com/52669dec-2fd7-4f3e-b322-e93d9da5984d">IPNPXDeviceAssociation</a>
 

 

