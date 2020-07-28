---
UID: NF:strmif.IDvdInfo2.GetDefaultSubpictureLanguage
title: IDvdInfo2::GetDefaultSubpictureLanguage (strmif.h)
description: The GetDefaultSubpictureLanguage method retrieves the default subpicture language.
helpviewer_keywords: ["GetDefaultSubpictureLanguage","GetDefaultSubpictureLanguage method [DirectShow]","GetDefaultSubpictureLanguage method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDefaultSubpictureLanguage method","IDvdInfo2.GetDefaultSubpictureLanguage","IDvdInfo2::GetDefaultSubpictureLanguage","IDvdInfo2GetDefaultSubpictureLanguage","dshow.idvdinfo2_getdefaultsubpicturelanguage","strmif/IDvdInfo2::GetDefaultSubpictureLanguage"]
old-location: dshow\idvdinfo2_getdefaultsubpicturelanguage.htm
tech.root: dshow
ms.assetid: ada423a5-90ef-48e1-80fa-04d0a24da8f7
ms.date: 12/05/2018
ms.keywords: GetDefaultSubpictureLanguage, GetDefaultSubpictureLanguage method [DirectShow], GetDefaultSubpictureLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDefaultSubpictureLanguage method, IDvdInfo2.GetDefaultSubpictureLanguage, IDvdInfo2::GetDefaultSubpictureLanguage, IDvdInfo2GetDefaultSubpictureLanguage, dshow.idvdinfo2_getdefaultsubpicturelanguage, strmif/IDvdInfo2::GetDefaultSubpictureLanguage
f1_keywords:
- strmif/IDvdInfo2.GetDefaultSubpictureLanguage
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdInfo2.GetDefaultSubpictureLanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetDefaultSubpictureLanguage


## -description



The <code>GetDefaultSubpictureLanguage</code> method retrieves the default subpicture language.




## -parameters




### -param pLanguage [out]

Receives the language information.


### -param pSubpictureExtension [out]

Pointer to a variable of type [DVD_SUBPICTURE_LANG_EXT](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_subpicture_lang_ext) that receives one of the allowable values indicating the default language extension.


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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

