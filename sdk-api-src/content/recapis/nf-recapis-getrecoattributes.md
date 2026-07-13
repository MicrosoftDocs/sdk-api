---
UID: NF:recapis.GetRecoAttributes
title: GetRecoAttributes function (recapis.h)
description: Retrieves the attributes of the recognizer.
helpviewer_keywords: ["45683203-1886-4542-8b66-84861862cb6a","GetRecoAttributes","GetRecoAttributes function [Tablet PC]","recapis/GetRecoAttributes","tablet.getrecoattributes"]
old-location: tablet\getrecoattributes.htm
tech.root: tablet
ms.assetid: 45683203-1886-4542-8b66-84861862cb6a
ms.date: 12/05/2018
ms.keywords: 45683203-1886-4542-8b66-84861862cb6a, GetRecoAttributes, GetRecoAttributes function [Tablet PC], recapis/GetRecoAttributes, tablet.getrecoattributes
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRecoAttributes
 - recapis/GetRecoAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetRecoAttributes
---

# GetRecoAttributes function


## -description

Retrieves the attributes of the recognizer.

## -parameters

### -param hrec

Handle to the recognizer.

### -param pRecoAttrs

The attributes of the recognizer. The attributes define the languages and capabilities that the recognizer supports. For more information, see the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_attrs">RECO_ATTRS</a> structure.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

A gesture recognizer should set the RF_OBJECT bit of the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_attrs">RECO_ATTRS</a><b>::dwRecoCapabilityFlags</b> and should set every element in the <b>RECO_ATTRS</b><b>::awLanguageID</b> array to zero.

A gesture recognizer does not normally use a recognition guide. A gesture recognizer with no guide should clear the RF_LINED_INPUT and RF_BOXED_INPUT bits.

The <i>awcFriendlyName</i> parameter of the <a href="/windows/desktop/api/rectypes/ns-rectypes-reco_attrs">RECO_ATTRS</a> structure may be empty (that is, having the first element set to the null character) when you use this structure as a return value from the <b>GetRecoAttributes Function</b>. Because this is not an error, the return code for <i>awcFriendlyName</i> in <b>GetRecoAttributes Function</b> will be S_OK, and the other fields will contain data.

## -see-also

<a href="/windows/desktop/api/rectypes/ns-rectypes-reco_attrs">RECO_ATTRS Structure</a>