---
UID: NF:ocidl.IPropertyPageSite.GetLocaleID
title: IPropertyPageSite::GetLocaleID (ocidl.h)
description: Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.
helpviewer_keywords: ["GetLocaleID","GetLocaleID method [COM]","GetLocaleID method [COM]","IPropertyPageSite interface","IPropertyPageSite interface [COM]","GetLocaleID method","IPropertyPageSite.GetLocaleID","IPropertyPageSite::GetLocaleID","_ctrl_ipropertypagesite_getlocaleid","com.ipropertypagesite_getlocaleid","ocidl/IPropertyPageSite::GetLocaleID"]
old-location: com\ipropertypagesite_getlocaleid.htm
tech.root: com
ms.assetid: d569346d-4a40-42a4-ac8e-539588c4dd66
ms.date: 12/05/2018
ms.keywords: GetLocaleID, GetLocaleID method [COM], GetLocaleID method [COM],IPropertyPageSite interface, IPropertyPageSite interface [COM],GetLocaleID method, IPropertyPageSite.GetLocaleID, IPropertyPageSite::GetLocaleID, _ctrl_ipropertypagesite_getlocaleid, com.ipropertypagesite_getlocaleid, ocidl/IPropertyPageSite::GetLocaleID
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
 - IPropertyPageSite::GetLocaleID
 - ocidl/IPropertyPageSite::GetLocaleID
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
 - IPropertyPageSite.GetLocaleID
---

# IPropertyPageSite::GetLocaleID


## -description

Retrieves the locale identifier (an LCID) that a property page can use to adjust its locale-specific settings.

## -parameters

### -param pLocaleID [out]

A pointer to a variable that receives the locale identifier. See <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pLocaleID</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>



<a href="/windows/desktop/api/olectl/ns-olectl-ocpfiparams">OCPFIPARAMS</a>



<a href="/windows/desktop/api/ocidl/ns-ocidl-proppageinfo">PROPPAGEINFO</a>