---
UID: NF:strmif.IDvdInfo2.GetAudioLanguage
title: IDvdInfo2::GetAudioLanguage method
author: windows-driver-content
description: The GetAudioLanguage method retrieves the language of the specified audio stream within the current title.
old-location: dshow\idvdinfo2_getaudiolanguage.htm
old-project: DirectShow
ms.assetid: c95afa36-879b-4fd5-bf92-0b9b93c708ef
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetAudioLanguage method [DirectShow], GetAudioLanguage method [DirectShow], IDvdInfo2 interface, GetAudioLanguage,IDvdInfo2.GetAudioLanguage, IDvdInfo2, IDvdInfo2 interface [DirectShow], GetAudioLanguage method, IDvdInfo2::GetAudioLanguage, IDvdInfo2GetAudioLanguage, dshow.idvdinfo2_getaudiolanguage, strmif/IDvdInfo2::GetAudioLanguage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetAudioLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetAudioLanguage method


## -description



The <code>GetAudioLanguage</code> method retrieves the language of the specified audio stream within the current title.




## -parameters




### -param ulStream [in]

Audio stream number for the language being retrieved.


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
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

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
 




## -remarks



This method does not return languages for menus. It sets the value pointed to by <i>pLanguage</i> to zero if the stream contains an unknown language. Call the <b>GetLocaleInfo</b> function to create a human-readable string name from <i>pLanguage</i>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LCID Language;
hr = pDvdInfo-&gt;GetAudioLanguage(ulStream, &amp;Language);
if (SUCCEEDED(hr))
{
    int cchSize = GetLocaleInfo(Language, LOCALE_SENGLANGUAGE, 0, 0);
    TCHAR *szString = new TCHAR[cchSize];
    if (szString)
    {
        GetLocaleInfo(Language, LOCALE_SENGLANGUAGE, szString, cchSize);
        /* ... */
        delete [] szString;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

