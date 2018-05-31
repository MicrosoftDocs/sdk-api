---
UID: NF:strmif.IDvdControl2.SelectDefaultAudioLanguage
title: IDvdControl2::SelectDefaultAudioLanguage
author: windows-sdk-content
description: The SelectDefaultAudioLanguage method sets the default audio language.
old-location: dshow\idvdcontrol2_selectdefaultaudiolanguage.htm
old-project: DirectShow
ms.assetid: 1f5cf846-6f14-4c17-bd01-6a8ecb46fdab
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectDefaultAudioLanguage method, IDvdControl2.SelectDefaultAudioLanguage, IDvdControl2::SelectDefaultAudioLanguage, IDvdControl2SelectDefaultAudioLanguage, SelectDefaultAudioLanguage, SelectDefaultAudioLanguage method [DirectShow], SelectDefaultAudioLanguage method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectdefaultaudiolanguage, strmif/IDvdControl2::SelectDefaultAudioLanguage
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
-	IDvdControl2.SelectDefaultAudioLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SelectDefaultAudioLanguage


## -description



The <code>SelectDefaultAudioLanguage</code> method sets the default audio language.




## -parameters




### -param Language [in]

Locale identifier that specifies the default language.


### -param audioExtension [in]


<a href="https://msdn.microsoft.com/01d82199-18e1-4d84-add1-f4f6790155c8">DVD_AUDIO_LANG_EXT</a> enumeration that specifies the default audio language extension.


## -returns



Returns one of the following values.

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
The <i>audioExtension</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter is not in the Stop domain.

</td>
</tr>
</table>
 




## -remarks



This method selects the default language and language extensions to use when the disc is played. For example, if <i>Language</i> is specified as 0x409 for English and <i>audioExtension</i> is specified as DVD_AUD_EXT_NotSpecified, the DVD Navigator will look for the basic audio stream in English. If <i>audioExtension</i> is specified as DVD_AUD_EXT_VisuallyImpaired, the DVD Navigator will first look for a special audio stream in English for people with low vision. If the default stream is not found on a disc, the DVD Navigator will select the closest match.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>
              Annex J Command Name
            </td>
<td>
              Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

