---
UID: NF:strmif.IDvdInfo2.GetDVDTextLanguageInfo
title: IDvdInfo2::GetDVDTextLanguageInfo
author: windows-sdk-content
description: The GetDVDTextLanguageInfo method retrieves information about the text strings for a specified language. The method retrieves the number of strings for that language, the locale identifier, and the character set.
old-location: dshow\idvdinfo2_getdvdtextlanguageinfo.htm
old-project: DirectShow
ms.assetid: af8662af-f306-4142-b563-3b40a98b7fbe
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetDVDTextLanguageInfo, GetDVDTextLanguageInfo method [DirectShow], GetDVDTextLanguageInfo method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextLanguageInfo method, IDvdInfo2.GetDVDTextLanguageInfo, IDvdInfo2::GetDVDTextLanguageInfo, IDvdInfo2GetDVDTextLanguageInfo, dshow.idvdinfo2_getdvdtextlanguageinfo, strmif/IDvdInfo2::GetDVDTextLanguageInfo
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetDVDTextLanguageInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDVDTextLanguageInfo


## -description



The <code>GetDVDTextLanguageInfo</code> method retrieves information about the text strings for a specified language. The method retrieves the number of strings for that language, the locale identifier, and the character set.




## -parameters




### -param ulLangIndex [in]

Zero-based index of the language to query. To find the number of text-string languages on the DVD, call <a href="https://msdn.microsoft.com/20c6ee1f-f20b-40c5-bc84-5ec1c07c0681">IDvdInfo2::GetDVDTextNumberOfLanguages</a>.


### -param pulNumOfStrings [out]

Receives the number of text strings for the specified language.


### -param pLangCode [out]

Receives a <i>locale identifier</i> (LCID) that specifies the language in which the text is written. For example, the LCID for "en-us" is 0x0409.


### -param pbCharacterSet [out]

Receives a member of the <a href="https://msdn.microsoft.com/ee7d09e1-6274-4993-914e-d8f5efeb5f90">DVD_TextCharSet</a> enumeration. The value specifies the character set of the text string.


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
This DVD does not have any text strings, or the <i>ulLangIndex</i> parameter is out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal error occurred.

</td>
</tr>
</table>
 




## -remarks



To get a particular text string, call <a href="https://msdn.microsoft.com/e13d4212-0e4a-40cf-89c7-f0c22f5a5cb9">IDvdInfo2::GetDVDTextStringAsUnicode</a> or <a href="https://msdn.microsoft.com/a162b4ad-28f2-49fc-9b32-72538be9ddd5">IDvdInfo2::GetDVDTextStringAsNative</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>



<a href="https://msdn.microsoft.com/6d415ebb-5cd0-4631-9404-f2ebabef2476">Working with DVD Text Strings</a>
 

 

