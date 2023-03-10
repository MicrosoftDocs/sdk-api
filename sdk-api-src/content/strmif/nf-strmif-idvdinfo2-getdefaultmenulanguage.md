---
UID: NF:strmif.IDvdInfo2.GetDefaultMenuLanguage
title: IDvdInfo2::GetDefaultMenuLanguage (strmif.h)
description: The GetDefaultMenuLanguage method retrieves the default menu language.
helpviewer_keywords: ["GetDefaultMenuLanguage","GetDefaultMenuLanguage method [DirectShow]","GetDefaultMenuLanguage method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDefaultMenuLanguage method","IDvdInfo2.GetDefaultMenuLanguage","IDvdInfo2::GetDefaultMenuLanguage","IDvdInfo2GetDefaultMenuLanguage","dshow.idvdinfo2_getdefaultmenulanguage","strmif/IDvdInfo2::GetDefaultMenuLanguage"]
old-location: dshow\idvdinfo2_getdefaultmenulanguage.htm
tech.root: dshow
ms.assetid: f2ad5bec-fc8c-4fcf-8657-aa1726c28cdc
ms.date: 12/05/2018
ms.keywords: GetDefaultMenuLanguage, GetDefaultMenuLanguage method [DirectShow], GetDefaultMenuLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDefaultMenuLanguage method, IDvdInfo2.GetDefaultMenuLanguage, IDvdInfo2::GetDefaultMenuLanguage, IDvdInfo2GetDefaultMenuLanguage, dshow.idvdinfo2_getdefaultmenulanguage, strmif/IDvdInfo2::GetDefaultMenuLanguage
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2::GetDefaultMenuLanguage
 - strmif/IDvdInfo2::GetDefaultMenuLanguage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetDefaultMenuLanguage
---

# IDvdInfo2::GetDefaultMenuLanguage


## -description

The <code>GetDefaultMenuLanguage</code> method retrieves the default menu language.

## -parameters

### -param pLanguage [out]

Receives the language information.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pLanguage</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
DVD Navigator is not in a valid domain.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>