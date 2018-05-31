---
UID: NF:strmif.IDvdInfo2.GetSubpictureLanguage
title: IDvdInfo2::GetSubpictureLanguage
author: windows-sdk-content
description: The GetSubpictureLanguage method retrieves the language of the specified subpicture stream within the current title.
old-location: dshow\idvdinfo2_getsubpicturelanguage.htm
old-project: DirectShow
ms.assetid: 175ab238-59a9-4142-921b-ed374423f4e3
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetSubpictureLanguage, GetSubpictureLanguage method [DirectShow], GetSubpictureLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetSubpictureLanguage method, IDvdInfo2.GetSubpictureLanguage, IDvdInfo2::GetSubpictureLanguage, IDvdInfo2GetSubpictureLanguage, dshow.idvdinfo2_getsubpicturelanguage, strmif/IDvdInfo2::GetSubpictureLanguage
ms.prod: windows
ms.technology: windows-sdk
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
-	IDvdInfo2.GetSubpictureLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetSubpictureLanguage


## -description



The <code>GetSubpictureLanguage</code> method retrieves the language of the specified subpicture stream within the current title.




## -parameters




### -param ulStream [in]

Number of the subpicture stream for which the language is being retrieved.


### -param pLanguage [out]

Pointer to an LCID that receives the locale information. The language information can then be extracted from the LCID by using the Win32 <b>MAKELANGID</b> macro.


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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized or not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



To get the text languages available for a menu, call <a href="https://msdn.microsoft.com/97c95208-e2fc-4c9a-b8ba-61419b96aec9">GetMenuLanguages</a>. <code>GetSubpictureLanguage</code> sets the value pointed to by <i>pLanguage</i> to zero if the stream contains an unknown language. Call the Win32 <b>GetLocaleInfo</b> function as follows to create a human-readable string name from <i>pLanguage</i>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LCID Language;
hr = pDvdInfo-&gt;GetSubpictureLanguage(ulStream, &amp;Language);
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
 

 

