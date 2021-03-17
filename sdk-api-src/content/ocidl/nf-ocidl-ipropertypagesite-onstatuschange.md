---
UID: NF:ocidl.IPropertyPageSite.OnStatusChange
title: IPropertyPageSite::OnStatusChange (ocidl.h)
description: Informs the frame that the property page managed by this site has changed its state, that is, one or more property values have been changed in the page. Property pages should call this method whenever changes occur in their dialog boxes.
helpviewer_keywords: ["IPropertyPageSite interface [COM]","OnStatusChange method","IPropertyPageSite.OnStatusChange","IPropertyPageSite::OnStatusChange","OnStatusChange","OnStatusChange method [COM]","OnStatusChange method [COM]","IPropertyPageSite interface","PROPPAGESTATUS_DIRTY","PROPPAGESTATUS_VALIDATE","_ctrl_ipropertypagesite_onstatuschange","com.ipropertypagesite_onstatuschange","ocidl/IPropertyPageSite::OnStatusChange"]
old-location: com\ipropertypagesite_onstatuschange.htm
tech.root: com
ms.assetid: cea36260-b0f6-489a-b02a-3ca3576c6431
ms.date: 12/05/2018
ms.keywords: IPropertyPageSite interface [COM],OnStatusChange method, IPropertyPageSite.OnStatusChange, IPropertyPageSite::OnStatusChange, OnStatusChange, OnStatusChange method [COM], OnStatusChange method [COM],IPropertyPageSite interface, PROPPAGESTATUS_DIRTY, PROPPAGESTATUS_VALIDATE, _ctrl_ipropertypagesite_onstatuschange, com.ipropertypagesite_onstatuschange, ocidl/IPropertyPageSite::OnStatusChange
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPropertyPageSite::OnStatusChange
 - ocidl/IPropertyPageSite::OnStatusChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPageSite.OnStatusChange
---

# IPropertyPageSite::OnStatusChange


## -description

Informs the frame that the property page managed by this site has changed its state, that is, one or more property values have been changed in the page. Property pages should call this method whenever changes occur in their dialog boxes.

## -parameters

### -param dwFlags [in]

Indicates the changes that have occurred. This parameter can contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPPAGESTATUS_DIRTY"></a><a id="proppagestatus_dirty"></a><dl>
<dt><b>PROPPAGESTATUS_DIRTY</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The values in the pages have changed, so the state of the <b>Apply</b> button should be updated.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPPAGESTATUS_VALIDATE"></a><a id="proppagestatus_validate"></a><dl>
<dt><b>PROPPAGESTATUS_VALIDATE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Now is an appropriate time to apply changes.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG and S_OK.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>