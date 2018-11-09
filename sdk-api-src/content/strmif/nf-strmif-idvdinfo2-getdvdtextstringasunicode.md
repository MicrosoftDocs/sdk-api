---
UID: NF:strmif.IDvdInfo2.GetDVDTextStringAsUnicode
title: IDvdInfo2::GetDVDTextStringAsUnicode
author: windows-sdk-content
description: The GetDVDTextStringAsUnicode method retrieves a DVD text string for a specified language, and returns the text string as a Unicode string.
old-location: dshow\idvdinfo2_getdvdtextstringasunicode.htm
tech.root: DirectShow
ms.assetid: e13d4212-0e4a-40cf-89c7-f0c22f5a5cb9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetDVDTextStringAsUnicode, GetDVDTextStringAsUnicode method [DirectShow], GetDVDTextStringAsUnicode method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDTextStringAsUnicode method, IDvdInfo2.GetDVDTextStringAsUnicode, IDvdInfo2::GetDVDTextStringAsUnicode, IDvdInfo2GetDVDTextStringAsUnicode, dshow.idvdinfo2_getdvdtextstringasunicode, strmif/IDvdInfo2::GetDVDTextStringAsUnicode
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
 - IDvdInfo2.GetDVDTextStringAsUnicode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetDVDTextStringAsUnicode


## -description



The <code>GetDVDTextStringAsUnicode</code> method retrieves a DVD text string for a specified language, and returns the text string as a Unicode string.




## -parameters




### -param ulLangIndex [in]

Zero-based index of the language. To find the number of text-string languages on the DVD, call <a href="https://msdn.microsoft.com/20c6ee1f-f20b-40c5-bc84-5ec1c07c0681">IDvdInfo2::GetDVDTextNumberOfLanguages</a>.


### -param ulStringIndex [in]

Zero-based index of the string to retrieve. To find the number of strings for a given language, call <a href="https://msdn.microsoft.com/af8662af-f306-4142-b563-3b40a98b7fbe">IDvdInfo2::GetDVDTextLanguageInfo</a>.


### -param pchwBuffer

TBD


### -param ulMaxBufferSize [in]

Size of the <i>pchBuffer</i> buffer, in <b>WCHARs</b>.


### -param pulActualSize [out]

Receives the actual length of the string in characters, including the terminating <b>NULL</b>.


### -param arg6 [out]

Receives a member of the <a href="https://msdn.microsoft.com/e8308432-a9a1-40d5-abec-aa6f86af9e5b">DVD_TextStringType</a> enumeration. The value indicates the type of text string, such as movie title or song name. This parameter can also receive values that are not defined in the <b>DVD_TextStringType</b> enumeration.


#### - pchBuffer [out]

Pointer to a buffer that receives the text string. If <i>pchBuffer</i> is <b>NULL</b>, this method returns the size of the string in <i>pulActualSize</i>.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unsupported te

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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



This method supports text strings that are encoded as Unicode or 7-bit ASCII (ISO/IEC 646). If the text string uses ASCII encoding, the method converts the string to a wide-character string. If the text string uses any other character set, the method returns E_FAIL. In that case, you can call <a href="https://msdn.microsoft.com/a162b4ad-28f2-49fc-9b32-72538be9ddd5">IDvdInfo2::GetDVDTextStringAsNative</a> to retrieve the string as a raw byte array. To find the character set, call <a href="https://msdn.microsoft.com/af8662af-f306-4142-b563-3b40a98b7fbe">IDvdInfo2::GetDVDTextLanguageInfo</a>.

The returned string always includes a terminating <b>NULL</b>. If the buffer is smaller than the length of the DVD text string, the string is truncated. To find the required size of the buffer, call the method once with <i>pchBuffer</i> equal to <b>NULL</b> and <i>ulMaxBufferSize</i> equal to zero. The size is returned in <i>pulActualSize</i>. Then allocate a buffer and call the method again.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>



<a href="https://msdn.microsoft.com/6d415ebb-5cd0-4631-9404-f2ebabef2476">Working with DVD Text Strings</a>
 

 

