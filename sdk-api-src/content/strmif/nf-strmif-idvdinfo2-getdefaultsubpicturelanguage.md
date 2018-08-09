---
UID: NF:strmif.IDvdInfo2.GetDefaultSubpictureLanguage
title: IDvdInfo2::GetDefaultSubpictureLanguage
author: windows-sdk-content
description: The GetDefaultSubpictureLanguage method retrieves the default subpicture language.
old-location: dshow\idvdinfo2_getdefaultsubpicturelanguage.htm
old-project: DirectShow
ms.assetid: ada423a5-90ef-48e1-80fa-04d0a24da8f7
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetDefaultSubpictureLanguage, GetDefaultSubpictureLanguage method [DirectShow], GetDefaultSubpictureLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDefaultSubpictureLanguage method, IDvdInfo2.GetDefaultSubpictureLanguage, IDvdInfo2::GetDefaultSubpictureLanguage, IDvdInfo2GetDefaultSubpictureLanguage, dshow.idvdinfo2_getdefaultsubpicturelanguage, strmif/IDvdInfo2::GetDefaultSubpictureLanguage
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
 - IDvdInfo2.GetDefaultSubpictureLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDefaultSubpictureLanguage


## -description



The <code>GetDefaultSubpictureLanguage</code> method retrieves the default subpicture language.




## -parameters




### -param pLanguage [out]

Receives the language information.


### -param pSubpictureExtension [out]

Pointer to a variable of type <a href="https://msdn.microsoft.com/314c6187-a475-44c9-b22a-b168211fceb3">DVD_SUBPICTURE_LANG_EXT</a> that receives one of the allowable values indicating the default language extension.


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
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

