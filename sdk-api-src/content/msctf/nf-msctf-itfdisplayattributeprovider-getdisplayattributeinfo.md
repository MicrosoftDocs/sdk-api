---
UID: NF:msctf.ITfDisplayAttributeProvider.GetDisplayAttributeInfo
title: ITfDisplayAttributeProvider::GetDisplayAttributeInfo (msctf.h)
description: ITfDisplayAttributeProvider::GetDisplayAttributeInfo method
helpviewer_keywords: ["GetDisplayAttributeInfo","GetDisplayAttributeInfo method [Text Services Framework]","GetDisplayAttributeInfo method [Text Services Framework]","ITfDisplayAttributeProvider interface","ITfDisplayAttributeProvider interface [Text Services Framework]","GetDisplayAttributeInfo method","ITfDisplayAttributeProvider.GetDisplayAttributeInfo","ITfDisplayAttributeProvider::GetDisplayAttributeInfo","_tsf_itfdisplayattributeprovider_getdisplayattributeinfo_ref","msctf/ITfDisplayAttributeProvider::GetDisplayAttributeInfo","tsf.itfdisplayattributeprovider_getdisplayattributeinfo"]
old-location: tsf\itfdisplayattributeprovider_getdisplayattributeinfo.htm
tech.root: TSF
ms.assetid: 2081f1b4-45b4-43bd-ba20-392a5ad0a30e
ms.date: 12/05/2018
ms.keywords: GetDisplayAttributeInfo, GetDisplayAttributeInfo method [Text Services Framework], GetDisplayAttributeInfo method [Text Services Framework],ITfDisplayAttributeProvider interface, ITfDisplayAttributeProvider interface [Text Services Framework],GetDisplayAttributeInfo method, ITfDisplayAttributeProvider.GetDisplayAttributeInfo, ITfDisplayAttributeProvider::GetDisplayAttributeInfo, _tsf_itfdisplayattributeprovider_getdisplayattributeinfo_ref, msctf/ITfDisplayAttributeProvider::GetDisplayAttributeInfo, tsf.itfdisplayattributeprovider_getdisplayattributeinfo
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
 - ITfDisplayAttributeProvider::GetDisplayAttributeInfo
 - msctf/ITfDisplayAttributeProvider::GetDisplayAttributeInfo
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
 - ITfDisplayAttributeProvider.GetDisplayAttributeInfo
---

# ITfDisplayAttributeProvider::GetDisplayAttributeInfo


## -description

Obtains a display attribute provider object for a particular display attribute.

## -parameters

### -param guid [in]

Contains a GUID value that identifies the display attribute to obtain the display attribute information object for. The text service must publish these values and what they indicate. This identifier can also be obtained by enumerating the display attributes for a range of text.

### -param ppInfo [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo</a> interface pointer that receives the display attribute information object.

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
One or more parameters are invalid.

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

<a href="/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeprovider">ITfDisplayAttributeProvider</a>



<a href="/windows/desktop/TSF/providing-display-attributes">Providing Display Attributes</a>