---
UID: NF:ctfutb.IEnumTfLangBarItems.Next
title: IEnumTfLangBarItems::Next (ctfutb.h)
description: IEnumTfLangBarItems::Next method
helpviewer_keywords: ["IEnumTfLangBarItems interface [Text Services Framework]","Next method","IEnumTfLangBarItems.Next","IEnumTfLangBarItems::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfLangBarItems interface","_tsf_ienumtflangbaritems_next_ref","ctfutb/IEnumTfLangBarItems::Next","tsf.ienumtflangbaritems_next"]
old-location: tsf\ienumtflangbaritems_next.htm
tech.root: TSF
ms.assetid: 46e24685-581c-4c68-80df-4465e90e3e36
ms.date: 12/05/2018
ms.keywords: IEnumTfLangBarItems interface [Text Services Framework],Next method, IEnumTfLangBarItems.Next, IEnumTfLangBarItems::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfLangBarItems interface, _tsf_ienumtflangbaritems_next_ref, ctfutb/IEnumTfLangBarItems::Next, tsf.ienumtflangbaritems_next
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfLangBarItems::Next
 - ctfutb/IEnumTfLangBarItems::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfLangBarItems.Next
---

# IEnumTfLangBarItems::Next


## -description

Obtains the specified number of elements in the enumeration sequence from the current position.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param ppItem [out]

Pointer to an array of <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched

[in, out] Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppItem</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-ienumtflangbaritems">IEnumTfLangBarItems</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>