---
UID: NF:pnpxassoc.IPNPXAssociation.Delete
title: IPNPXAssociation::Delete (pnpxassoc.h)
description: Removes an entry from the association database.
helpviewer_keywords: ["Delete","Delete method","Delete method","IPNPXAssociation interface","IPNPXAssociation interface","Delete method","IPNPXAssociation.Delete","IPNPXAssociation::Delete","ncd.ipnpxassociation_delete","pnpxassoc/IPNPXAssociation::Delete"]
old-location: ncd\ipnpxassociation_delete.htm
tech.root: ncd
ms.assetid: cc00c135-140d-4e05-9180-779917d88688
ms.date: 12/05/2018
ms.keywords: Delete, Delete method, Delete method,IPNPXAssociation interface, IPNPXAssociation interface,Delete method, IPNPXAssociation.Delete, IPNPXAssociation::Delete, ncd.ipnpxassociation_delete, pnpxassoc/IPNPXAssociation::Delete
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
 - IPNPXAssociation::Delete
 - pnpxassoc/IPNPXAssociation::Delete
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
 - IPNPXAssociation.Delete
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

This method modifies the association database entry corresponding to the function instance from which the <a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxassociation">IPNPXAssociation</a> interface was obtained. 

To mark a device as unavailable for use without deleting the association database entry, call <a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxassociation-unassociate">IPNPXAssociation::Unassociate</a>.

## -see-also

<a href="/windows/desktop/api/pnpxassoc/nn-pnpxassoc-ipnpxassociation">IPNPXAssociation</a>



<a href="/windows/desktop/api/pnpxassoc/nf-pnpxassoc-ipnpxdeviceassociation-delete">IPNPXDeviceAssociation::Delete</a>