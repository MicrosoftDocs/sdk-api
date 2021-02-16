---
UID: NF:oleidl.IOleLink.Update
title: IOleLink::Update (oleidl.h)
description: Updates the compound document's cached data for a linked object. This involves binding to the link source, if it is not already bound.
helpviewer_keywords: ["IOleLink interface [COM]","Update method","IOleLink.Update","IOleLink::Update","Update","Update method [COM]","Update method [COM]","IOleLink interface","_ole_iolelink_update","com.iolelink_update","oleidl/IOleLink::Update"]
old-location: com\iolelink_update.htm
tech.root: com
ms.assetid: c1da8b95-88e7-42b0-884c-5aa394cc49f4
ms.date: 12/05/2018
ms.keywords: IOleLink interface [COM],Update method, IOleLink.Update, IOleLink::Update, Update, Update method [COM], Update method [COM],IOleLink interface, _ole_iolelink_update, com.iolelink_update, oleidl/IOleLink::Update
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleLink::Update
 - oleidl/IOleLink::Update
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleLink.Update
---

# IOleLink::Update


## -description

Updates the compound document's cached data for a linked object. This involves binding to the link source, if it is not already bound.

## -parameters

### -param pbc [in]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface on the bind context to be used in binding the link source. This parameter can be <b>NULL</b>. The bind context caches objects bound during the binding process, contains parameters that apply to all operations using the bind context, and provides the means by which the binding implementation should retrieve information about its environment. For more information, see <b>IBindCtx</b>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_E_NOCACHE_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
The bind operation worked but no caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_SOMECACHES_NOTUPDATED</b></dt>
</dl>
</td>
<td width="60%">
The bind operation worked but not all caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Unable to bind to the link source.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application should call <b>Update</b> if the end user updates the cached data for a linked object.

The end user can update the cached data for a linked object by choosing the <b>Update Now</b> button in the <b>Links</b> dialog box. If you use the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> function to display the <b>Links</b> dialog box, you must implement the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. The dialog box calls your implementations of <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-updatelink">IOleUILinkContainer::UpdateLink</a> when the end user chooses the <b>Update Now</b> button. Your implementation of that method can call <b>Update</b>.

Your container application can also call <b>Update</b> to update a linked object, because that method calls <b>Update</b> when it is called on a linked object.

This method updates both automatic links and manual links. For manual links, calling <b>Update</b> or <b>Update</b> is the only way to update the caches. For more information on automatic and manual links, see <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a>.

<h3><a id="Notes_on_Implementation"></a><a id="notes_on_implementation"></a><a id="NOTES_ON_IMPLEMENTATION"></a>Notes on Implementation</h3>
If <i>pbc</i> is non-<b>NULL</b>, the linked object's implementation of <b>Update</b> calls <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">IBindCtx::RegisterObjectBound</a> to register the bound link source. This ensures that the link source remains running until the bind context is released.

The current caches are left intact if the link source cannot be bound.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectbound">IBindCtx::RegisterObjectBound</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">IOleLink::SetUpdateOptions</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">IOleLink::Update</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>