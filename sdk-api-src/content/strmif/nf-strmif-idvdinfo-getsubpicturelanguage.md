---
UID: NF:strmif.IDvdInfo.GetSubpictureLanguage
title: IDvdInfo::GetSubpictureLanguage
author: windows-driver-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the language of the specified subpicture stream within the current title.
old-location: dshow\idvdinfo_getsubpicturelanguage.htm
old-project: DirectShow
ms.assetid: f75ef36d-8556-4ca0-9f7f-6c09b86da24e
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetSubpictureLanguage, GetSubpictureLanguage method [DirectShow], GetSubpictureLanguage method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetSubpictureLanguage method, IDvdInfo.GetSubpictureLanguage, IDvdInfo::GetSubpictureLanguage, IDvdInfoGetSubpictureLanguage, dshow.idvdinfo_getsubpicturelanguage, strmif/IDvdInfo::GetSubpictureLanguage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdInfo.GetSubpictureLanguage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetSubpictureLanguage


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the language of the specified subpicture stream within the current title.




## -parameters




### -param ulStream




### -param pLanguage [out]

Pointer to the retrieved language.


#### - nStream [in]

Stream number.


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
Requested action is not supported on this domain (<a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>).

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



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

