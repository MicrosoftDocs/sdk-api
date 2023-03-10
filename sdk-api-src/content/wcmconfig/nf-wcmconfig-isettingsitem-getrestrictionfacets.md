---
UID: NF:wcmconfig.ISettingsItem.GetRestrictionFacets
title: ISettingsItem::GetRestrictionFacets (wcmconfig.h)
description: Gets the restrictions defined for this item.
helpviewer_keywords: ["GetRestrictionFacets","GetRestrictionFacets method [SMI]","GetRestrictionFacets method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetRestrictionFacets method","ISettingsItem.GetRestrictionFacets","ISettingsItem::GetRestrictionFacets","smi.isettingsitem_getrestrictionfacets","wcmconfig/ISettingsItem::GetRestrictionFacets"]
old-location: smi\isettingsitem_getrestrictionfacets.htm
tech.root: SMI
ms.assetid: 64cf82d5-c210-4ff2-a7c8-1a284859382e
ms.date: 12/05/2018
ms.keywords: GetRestrictionFacets, GetRestrictionFacets method [SMI], GetRestrictionFacets method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetRestrictionFacets method, ISettingsItem.GetRestrictionFacets, ISettingsItem::GetRestrictionFacets, smi.isettingsitem_getrestrictionfacets, wcmconfig/ISettingsItem::GetRestrictionFacets
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
 - ISettingsItem::GetRestrictionFacets
 - wcmconfig/ISettingsItem::GetRestrictionFacets
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
 - ISettingsItem.GetRestrictionFacets
---

# ISettingsItem::GetRestrictionFacets


## -description

Gets the restrictions defined for this item.

## -parameters

### -param RestrictionFacets [out]

A bitmask of  the <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmrestrictionfacets">WcmRestrictionFacets</a> values that are defined for this item.

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
Indicates that the item is not a scalar setting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is no value for the item.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>