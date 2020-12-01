---
UID: NF:msctf.ITfContextOwner.GetAttribute
title: ITfContextOwner::GetAttribute (msctf.h)
description: The ITfContextOwner::GetAttribute method returns the value of a supported attribute. If the attribute is unsupported, the pvarValue parameter is set to VT_EMPTY.
helpviewer_keywords: ["GetAttribute","GetAttribute method [Text Services Framework]","GetAttribute method [Text Services Framework]","ITfContextOwner interface","ITfContextOwner interface [Text Services Framework]","GetAttribute method","ITfContextOwner.GetAttribute","ITfContextOwner::GetAttribute","_tsf_itfcontextowner_getattribute_ref","msctf/ITfContextOwner::GetAttribute","tsf.itfcontextowner_getattribute"]
old-location: tsf\itfcontextowner_getattribute.htm
tech.root: TSF
ms.assetid: a249d529-fdb1-4f5f-84ae-f26dae917609
ms.date: 12/05/2018
ms.keywords: GetAttribute, GetAttribute method [Text Services Framework], GetAttribute method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetAttribute method, ITfContextOwner.GetAttribute, ITfContextOwner::GetAttribute, _tsf_itfcontextowner_getattribute_ref, msctf/ITfContextOwner::GetAttribute, tsf.itfcontextowner_getattribute
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwner::GetAttribute
 - msctf/ITfContextOwner::GetAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetAttribute
---

# ITfContextOwner::GetAttribute


## -description

The <b>ITfContextOwner::GetAttribute</b> method returns the value of a supported attribute. If the attribute is unsupported, the <i>pvarValue</i> parameter is set to VT_EMPTY.

## -parameters

### -param rguidAttribute [in]

Specifies the attribute GUID.

### -param pvarValue [out]

Receives the attribute value. If the attribute is unsupported, this parameter is set to VT_EMPTY.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

Context owners using the default text store of the TSF manager can implement a simplified version of attributes with this method. The supported attributes are application or text service dependent. For more information about predefined attributes recognized in TSF, see the following topics.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a>



<a href="/windows/desktop/TSF/other-predefined-attributes">Other Predefined Attributes</a>



<a href="/windows/desktop/TSF/predefined-font-attributes">Predefined Font Attributes</a>



<a href="/windows/desktop/TSF/predefined-list-attributes">Predefined List Attributes</a>



<a href="/windows/desktop/TSF/predefined-text-attributes">Predefined Text Attributes</a>