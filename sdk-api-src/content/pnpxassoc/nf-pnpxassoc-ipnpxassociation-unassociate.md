---
UID: NF:pnpxassoc.IPNPXAssociation.Unassociate
title: IPNPXAssociation::Unassociate (pnpxassoc.h)
description: Marks an association database entry as unassociated.
helpviewer_keywords: ["IPNPXAssociation interface","Unassociate method","IPNPXAssociation.Unassociate","IPNPXAssociation::Unassociate","Unassociate","Unassociate method","Unassociate method","IPNPXAssociation interface","ncd.ipnpxassociation_unassociate","pnpxassoc/IPNPXAssociation::Unassociate"]
old-location: ncd\ipnpxassociation_unassociate.htm
tech.root: ncd
ms.assetid: 92f0cc10-03a0-498f-acd1-4b03302aa33b
ms.date: 12/05/2018
ms.keywords: IPNPXAssociation interface,Unassociate method, IPNPXAssociation.Unassociate, IPNPXAssociation::Unassociate, Unassociate, Unassociate method, Unassociate method,IPNPXAssociation interface, ncd.ipnpxassociation_unassociate, pnpxassoc/IPNPXAssociation::Unassociate
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
 - IPNPXAssociation::Unassociate
 - pnpxassoc/IPNPXAssociation::Unassociate
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
 - IPNPXAssociation.Unassociate
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

This method modifies the association database entry corresponding to the function instance from which the <a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxassociation">IPNPXAssociation</a> interface was obtained. 

This method does not remove the entry from the association database. To remove an entry from the association database, call <a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxassociation-delete">IPNPXAssociation::Delete</a>.

## -see-also

<a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxassociation">IPNPXAssociation</a>



<a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-unassociate">IPNPXDeviceAssociation::Unassociate</a>