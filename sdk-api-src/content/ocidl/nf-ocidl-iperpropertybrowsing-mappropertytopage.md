---
UID: NF:ocidl.IPerPropertyBrowsing.MapPropertyToPage
title: IPerPropertyBrowsing::MapPropertyToPage (ocidl.h)
description: Retrieves the CLSID of the property page associated with the specified property.
helpviewer_keywords: ["IPerPropertyBrowsing interface [COM]","MapPropertyToPage method","IPerPropertyBrowsing.MapPropertyToPage","IPerPropertyBrowsing::MapPropertyToPage","MapPropertyToPage","MapPropertyToPage method [COM]","MapPropertyToPage method [COM]","IPerPropertyBrowsing interface","_ctrl_iperpropertybrowsing_mappropertytopage","com.iperpropertybrowsing_mappropertytopage","ocidl/IPerPropertyBrowsing::MapPropertyToPage"]
old-location: com\iperpropertybrowsing_mappropertytopage.htm
tech.root: com
ms.assetid: f8cf86eb-23d1-4aa6-859a-055df99b064c
ms.date: 12/05/2018
ms.keywords: IPerPropertyBrowsing interface [COM],MapPropertyToPage method, IPerPropertyBrowsing.MapPropertyToPage, IPerPropertyBrowsing::MapPropertyToPage, MapPropertyToPage, MapPropertyToPage method [COM], MapPropertyToPage method [COM],IPerPropertyBrowsing interface, _ctrl_iperpropertybrowsing_mappropertytopage, com.iperpropertybrowsing_mappropertytopage, ocidl/IPerPropertyBrowsing::MapPropertyToPage
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
 - IPerPropertyBrowsing::MapPropertyToPage
 - ocidl/IPerPropertyBrowsing::MapPropertyToPage
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
 - IPerPropertyBrowsing.MapPropertyToPage
---

# IPerPropertyBrowsing::MapPropertyToPage


## -description

Retrieves the CLSID of the property page associated with the specified property.

## -parameters

### -param dispID [in]

The dispatch identifier of the property.

### -param pClsid [out]

A pointer to the CLSID identifying the property page associated with the property specified by <i>dispID</i>. If this method fails, *<i>pClsid</i> is set to CLSID_NULL.

## -returns

This method can return the standard return values E_INVALIDARG and E_UNEXPECTED, as well as the following values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The object does not support property pages at all or does not support mapping properties to the page CLSID. In other words, this feature of specific property browsing is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pClsid</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The CLSID returned from this method can be passed to <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a> to specify the initial page to display in the property sheet.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>