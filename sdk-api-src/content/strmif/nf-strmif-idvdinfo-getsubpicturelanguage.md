---
UID: NF:strmif.IDvdInfo.GetSubpictureLanguage
title: IDvdInfo::GetSubpictureLanguage (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the language of the specified subpicture stream within the current title.
helpviewer_keywords: ["GetSubpictureLanguage","GetSubpictureLanguage method [DirectShow]","GetSubpictureLanguage method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetSubpictureLanguage method","IDvdInfo.GetSubpictureLanguage","IDvdInfo::GetSubpictureLanguage","IDvdInfoGetSubpictureLanguage","dshow.idvdinfo_getsubpicturelanguage","strmif/IDvdInfo::GetSubpictureLanguage"]
old-location: dshow\idvdinfo_getsubpicturelanguage.htm
tech.root: dshow
ms.assetid: f75ef36d-8556-4ca0-9f7f-6c09b86da24e
ms.date: 12/05/2018
ms.keywords: GetSubpictureLanguage, GetSubpictureLanguage method [DirectShow], GetSubpictureLanguage method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetSubpictureLanguage method, IDvdInfo.GetSubpictureLanguage, IDvdInfo::GetSubpictureLanguage, IDvdInfoGetSubpictureLanguage, dshow.idvdinfo_getsubpicturelanguage, strmif/IDvdInfo::GetSubpictureLanguage
f1_keywords:
- strmif/IDvdInfo.GetSubpictureLanguage
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IDvdInfo.GetSubpictureLanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetSubpictureLanguage


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the language of the specified subpicture stream within the current title.




## -parameters




### -param ulStream [in]

Stream number.


### -param pLanguage [out]

Pointer to the retrieved language.


## -returns



Returns an <b>HRESULT</b> value .

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>
 




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

This method does not return languages for menus. This method sets the value pointed to by <i>pLanguage</i> to zero if the stream does not include language. Call the Win32 <b>GetLocaleInfo</b> function as follows to create a human-readable string name from <i>pLanguage</i>. LOCALE_SENGLANGUAGE is the locale information type, pszString is a pointer to a buffer to receive the requested data, and cbSize specifies the size of pszString.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
GetLocaleInfo(*pLanguage, LOCALE_SENGLANGUAGE, pszString, cbSize);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

