---
UID: NF:strmif.IDvdInfo2.GetDefaultAudioLanguage
title: IDvdInfo2::GetDefaultAudioLanguage
author: windows-sdk-content
description: The GetDefaultAudioLanguage method retrieves the default audio language.
old-location: dshow\idvdinfo2_getdefaultaudiolanguage.htm
old-project: DirectShow
ms.assetid: 89f93521-9df7-4162-bb66-2210cceebc75
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetDefaultAudioLanguage, GetDefaultAudioLanguage method [DirectShow], GetDefaultAudioLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDefaultAudioLanguage method, IDvdInfo2.GetDefaultAudioLanguage, IDvdInfo2::GetDefaultAudioLanguage, IDvdInfo2GetDefaultAudioLanguage, dshow.idvdinfo2_getdefaultaudiolanguage, strmif/IDvdInfo2::GetDefaultAudioLanguage
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
 - IDvdInfo2.GetDefaultAudioLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDefaultAudioLanguage


## -description



The <code>GetDefaultAudioLanguage</code> method retrieves the default audio language.




## -parameters




### -param pLanguage [out]

Receives the default language information.


### -param pAudioExtension

Pointer to a variable of type <a href="https://msdn.microsoft.com/01d82199-18e1-4d84-add1-f4f6790155c8">DVD_AUDIO_LANG_EXT</a> that receives a value indicating the default DVD audio language extension.


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
 

 

