---
UID: NF:pnpxassoc.IPNPXAssociation.Unassociate
title: IPNPXAssociation::Unassociate
author: windows-sdk-content
description: Marks an association database entry as unassociated.
old-location: ncd\ipnpxassociation_unassociate.htm
tech.root: fundisc
ms.assetid: 92f0cc10-03a0-498f-acd1-4b03302aa33b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPNPXAssociation interface,Unassociate method, IPNPXAssociation.Unassociate, IPNPXAssociation::Unassociate, Unassociate, Unassociate method, Unassociate method,IPNPXAssociation interface, ncd.ipnpxassociation_unassociate, pnpxassoc/IPNPXAssociation::Unassociate
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
 - IPNPXAssociation.Unassociate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPNPXAssociation::Unassociate


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Marks an association database entry as unassociated.  If a function instance is unassociated, then it is a <i>not present</i> instance and the device corresponding to the function instance is not available for use.


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

This method does not remove the entry from the association database. To remove an entry from the association database, call <a href="https://msdn.microsoft.com/cc00c135-140d-4e05-9180-779917d88688">IPNPXAssociation::Delete</a>.




## -see-also




<a href="https://msdn.microsoft.com/03c1c4cb-fffb-4b4a-963a-200670062f4a">IPNPXAssociation</a>



<a href="https://msdn.microsoft.com/fb420967-c79c-4edd-a432-b982219c0746">IPNPXDeviceAssociation::Unassociate</a>
 

 

