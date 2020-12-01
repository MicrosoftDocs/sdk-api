---
UID: NF:msctf.ITfDisplayAttributeProvider.EnumDisplayAttributeInfo
title: ITfDisplayAttributeProvider::EnumDisplayAttributeInfo (msctf.h)
description: ITfDisplayAttributeProvider::EnumDisplayAttributeInfo method
helpviewer_keywords: ["EnumDisplayAttributeInfo","EnumDisplayAttributeInfo method [Text Services Framework]","EnumDisplayAttributeInfo method [Text Services Framework]","ITfDisplayAttributeProvider interface","ITfDisplayAttributeProvider interface [Text Services Framework]","EnumDisplayAttributeInfo method","ITfDisplayAttributeProvider.EnumDisplayAttributeInfo","ITfDisplayAttributeProvider::EnumDisplayAttributeInfo","_tsf_itfdisplayattributeprovider_enumdisplayattributeinfo_ref","msctf/ITfDisplayAttributeProvider::EnumDisplayAttributeInfo","tsf.itfdisplayattributeprovider_enumdisplayattributeinfo"]
old-location: tsf\itfdisplayattributeprovider_enumdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 1a19de91-ad79-4c75-956b-5f5de6700cbe
ms.date: 12/05/2018
ms.keywords: EnumDisplayAttributeInfo, EnumDisplayAttributeInfo method [Text Services Framework], EnumDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeProvider interface, ITfDisplayAttributeProvider interface [Text Services Framework],EnumDisplayAttributeInfo method, ITfDisplayAttributeProvider.EnumDisplayAttributeInfo, ITfDisplayAttributeProvider::EnumDisplayAttributeInfo, _tsf_itfdisplayattributeprovider_enumdisplayattributeinfo_ref, msctf/ITfDisplayAttributeProvider::EnumDisplayAttributeInfo, tsf.itfdisplayattributeprovider_enumdisplayattributeinfo
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Imjpcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDisplayAttributeProvider::EnumDisplayAttributeInfo
 - msctf/ITfDisplayAttributeProvider::EnumDisplayAttributeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imjpcic.dll
api_name:
 - ITfDisplayAttributeProvider.EnumDisplayAttributeInfo
---

# ITfDisplayAttributeProvider::EnumDisplayAttributeInfo


## -description

Obtains an enumerator that contains all display attribute info objects supported by the display attribute provider.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfdisplayattributeinfo">IEnumTfDisplayAttributeInfo</a> interface pointer that receives the enumerator object. The caller must release this interface when it is no longer required.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-ienumtfdisplayattributeinfo">IEnumTfDisplayAttributeInfo
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeprovider">ITfDisplayAttributeProvider</a>