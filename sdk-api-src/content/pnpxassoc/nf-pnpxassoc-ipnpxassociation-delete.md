---
UID: NF:pnpxassoc.IPNPXAssociation.Delete
title: IPNPXAssociation::Delete
author: windows-sdk-content
description: Removes an entry from the association database.
old-location: ncd\ipnpxassociation_delete.htm
tech.root: FunDisc
ms.assetid: cc00c135-140d-4e05-9180-779917d88688
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Delete, Delete method, Delete method,IPNPXAssociation interface, IPNPXAssociation interface,Delete method, IPNPXAssociation.Delete, IPNPXAssociation::Delete, ncd.ipnpxassociation_delete, pnpxassoc/IPNPXAssociation::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPNPXAssociation.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPNPXAssociation::Delete


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes an entry from the association database.


## -parameters




### -param pszSubcategory [in, optional]

The subcategory of the association database in which the entry is stored.  This parameter can be <b>NULL</b>.


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



This method modifies the association database entry corresponding to the function instance from which the <a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a> interface was obtained. 

To mark a device as unavailable for use without deleting the association database entry, call <a href="https://msdn.microsoft.com/92f0cc10-03a0-498f-acd1-4b03302aa33b">IPNPXAssociation::Unassociate</a>.




## -see-also




<a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a>



<a href="https://msdn.microsoft.com/208da586-6bb3-4365-90ba-9fd615a371eb">IPNPXDeviceAssociation::Delete</a>
 

 

