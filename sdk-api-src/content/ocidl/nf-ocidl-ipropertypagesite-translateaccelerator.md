---
UID: NF:ocidl.IPropertyPageSite.TranslateAccelerator
title: IPropertyPageSite::TranslateAccelerator (ocidl.h)
description: Passes a keystroke to the property frame for processing.
helpviewer_keywords: ["IPropertyPageSite interface [COM]","TranslateAccelerator method","IPropertyPageSite.TranslateAccelerator","IPropertyPageSite::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [COM]","TranslateAccelerator method [COM]","IPropertyPageSite interface","_ctrl_ipropertypagesite_translateaccelerator","com.ipropertypagesite_translateaccelerator","ocidl/IPropertyPageSite::TranslateAccelerator"]
old-location: com\ipropertypagesite_translateaccelerator.htm
tech.root: com
ms.assetid: d2233022-e66e-448c-a921-92948c05016f
ms.date: 12/05/2018
ms.keywords: IPropertyPageSite interface [COM],TranslateAccelerator method, IPropertyPageSite.TranslateAccelerator, IPropertyPageSite::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IPropertyPageSite interface, _ctrl_ipropertypagesite_translateaccelerator, com.ipropertypagesite_translateaccelerator, ocidl/IPropertyPageSite::TranslateAccelerator
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
 - IPropertyPageSite::TranslateAccelerator
 - ocidl/IPropertyPageSite::TranslateAccelerator
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
 - IPropertyPageSite.TranslateAccelerator
---

# IPropertyPageSite::TranslateAccelerator


## -description

Passes a keystroke to the property frame for processing.

## -parameters

### -param pMsg [in]

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure to be processed.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The page site did not process the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The page site does not support keyboard processing.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>