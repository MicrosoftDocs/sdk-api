---
UID: NF:wsdutil.WSDXMLCleanupElement
title: WSDXMLCleanupElement function (wsdutil.h)
description: Frees memory associated with an XML element.
helpviewer_keywords: ["WSDXMLCleanupElement","WSDXMLCleanupElement function","ncd.wsdxmlcleanupelement","wsdutil/WSDXMLCleanupElement"]
old-location: ncd\wsdxmlcleanupelement.htm
tech.root: ncd
ms.assetid: 5a421c9a-32c2-4eaf-84b9-6077afe9b82a
ms.date: 12/05/2018
ms.keywords: WSDXMLCleanupElement, WSDXMLCleanupElement function, ncd.wsdxmlcleanupelement, wsdutil/WSDXMLCleanupElement
req.header: wsdutil.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDXMLCleanupElement
 - wsdutil/WSDXMLCleanupElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDXMLCleanupElement
---

# WSDXMLCleanupElement function


## -description

Frees memory associated with an XML element.

## -parameters

### -param pAny [in]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

## -returns

This function can return one of these values.

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pAny</i> is <b>NULL</b>.

</td>
</tr>
</table>