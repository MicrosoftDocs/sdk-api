---
UID: NF:oleidl.IOleLink.SetUpdateOptions
title: IOleLink::SetUpdateOptions (oleidl.h)
description: Specifies how often a linked object should update its cached data.
helpviewer_keywords: ["IOleLink interface [COM]","SetUpdateOptions method","IOleLink.SetUpdateOptions","IOleLink::SetUpdateOptions","SetUpdateOptions","SetUpdateOptions method [COM]","SetUpdateOptions method [COM]","IOleLink interface","_ole_iolelink_setupdateoptions","com.iolelink_setupdateoptions","oleidl/IOleLink::SetUpdateOptions"]
old-location: com\iolelink_setupdateoptions.htm
tech.root: com
ms.assetid: 310c25b5-a2f6-4ed7-8673-c53809fad32f
ms.date: 12/05/2018
ms.keywords: IOleLink interface [COM],SetUpdateOptions method, IOleLink.SetUpdateOptions, IOleLink::SetUpdateOptions, SetUpdateOptions, SetUpdateOptions method [COM], SetUpdateOptions method [COM],IOleLink interface, _ole_iolelink_setupdateoptions, com.iolelink_setupdateoptions, oleidl/IOleLink::SetUpdateOptions
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
 - IOleLink::SetUpdateOptions
 - oleidl/IOleLink::SetUpdateOptions
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
 - IOleLink.SetUpdateOptions
---

# IOleLink::SetUpdateOptions


## -description

Specifies how often a linked object should update its cached data.

## -parameters

### -param dwUpdateOpt [in]

Specifies how often a linked object should update its cached data. The possible values for <i>dwUpdateOpt</i> are taken from the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-oleupdate">OLEUPDATE</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied value is invalid.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Your container application should call <b>IOleLink::SetUpdateOptions</b> when the end user changes the update option for a linked object.

The end user selects the update option for a linked object using the <b>Links</b> dialog box. If you use the <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a> function to display this dialog box, you must implement the <a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a> interface. The dialog box calls your <a href="/windows/desktop/api/oledlg/nf-oledlg-ioleuilinkcontainera-setlinkupdateoptions">IOleUILinkContainer::SetLinkUpdateOptions</a> method to specify the update option chosen by the end user. Your implementation of this method should call the <b>IOleLink::SetUpdateOptions</b> method to pass the selected option to the linked object.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The default update option is OLEUDPATE_ALWAYS. The linked object's implementation of <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a> saves the current update option.

If OLEUDPATE_ALWAYS is specified as the update option, the linked object updates the link's caches in the following situations:

<ul>
<li>When the update option is changed from manual to automatic, if the link source is running.</li>
<li>Whenever the linked object binds to the link source.</li>
<li>Whenever the link source is running and the linked object's <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a>, <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-save">IPersistStorage::Save</a>, or <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onsave">IAdviseSink::OnSave</a> implementations are called.</li>
</ul>
For both manual and automatic links, the linked object updates the cache whenever the container application calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">IOleLink::Update</a>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-getupdateoptions">IOleLink::GetUpdateOptions</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">IOleLink::Update</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-update">IOleObject::Update</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>