---
UID: NF:wcmconfig.ISettingsItem.CreateListElement
title: ISettingsItem::CreateListElement (wcmconfig.h)
description: Creates a new list element.
helpviewer_keywords: ["CreateListElement","CreateListElement method [SMI]","CreateListElement method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","CreateListElement method","ISettingsItem.CreateListElement","ISettingsItem::CreateListElement","smi.isettingsitem_createlistelement","wcmconfig/ISettingsItem::CreateListElement"]
old-location: smi\isettingsitem_createlistelement.htm
tech.root: SMI
ms.assetid: c18fd849-aaa5-49d0-9e72-b3134a6f2be8
ms.date: 12/05/2018
ms.keywords: CreateListElement, CreateListElement method [SMI], CreateListElement method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],CreateListElement method, ISettingsItem.CreateListElement, ISettingsItem::CreateListElement, smi.isettingsitem_createlistelement, wcmconfig/ISettingsItem::CreateListElement
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsItem::CreateListElement
 - wcmconfig/ISettingsItem::CreateListElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem.CreateListElement
---

# ISettingsItem::CreateListElement


## -description

Creates a new list element.

## -parameters

### -param KeyData [in]

The information for the key that defines the identity of the new list item. To determine the  correct value for the key data parameter, consult the information returned from <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getlistkeyinformation">ISettingsItem::GetListKeyInformation</a>. The variant obtained from <b>ISettingsItem::GetListKeyInformation</b> should be coercible to the type of the key. If the <b>ISettingsItem::GetListKeyInformation</b> method returns <b>S_FALSE</b>, use a string type for the key data.

### -param Child [out]

A pointer to the  newly created <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> list item.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is called on  an item that is not of setting type list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDVALUE, WCM_E_INVALIDVALUEFORMAT, or WCM_E_INVALIDDATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an attempt to create a list where the key cannot be coerced to the correct type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM </b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, either because  it is a read-only item, or because the namespace was opened in ReadOnly mode.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  When creating a scalar list item, you must set a value on the resulting <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> before releasing it, or it will not be persisted.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>