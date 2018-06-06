---
UID: NF:strmif.IDvdControl2.SelectDefaultSubpictureLanguage
title: IDvdControl2::SelectDefaultSubpictureLanguage
author: windows-sdk-content
description: The SelectDefaultSubpictureLanguage method sets the default language for subpicture text.
old-location: dshow\idvdcontrol2_selectdefaultsubpicturelanguage.htm
old-project: DirectShow
ms.assetid: f49698cd-cc83-4f05-991d-2b3bba77c33a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectDefaultSubpictureLanguage method, IDvdControl2.SelectDefaultSubpictureLanguage, IDvdControl2::SelectDefaultSubpictureLanguage, IDvdControl2SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage method [DirectShow], SelectDefaultSubpictureLanguage method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectdefaultsubpicturelanguage, strmif/IDvdControl2::SelectDefaultSubpictureLanguage
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
 - IDvdControl2.SelectDefaultSubpictureLanguage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl2::SelectDefaultSubpictureLanguage


## -description



The <code>SelectDefaultSubpictureLanguage</code> method sets the default language for subpicture text.




## -parameters




### -param Language [in]

Locale identifier that specifies the default language.


### -param subpictureExtension [in]


<a href="https://msdn.microsoft.com/314c6187-a475-44c9-b22a-b168211fceb3">DVD_SUBPICTURE_LANG_EXT</a> enumeration that specifies the default subpicture extension.


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
<i>Language</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



This method selects the default language and format to use for subpictures and menus when the disc is played. For example, if <i>Language</i> is specified as 0x409 for U.S. English and <i>subpictureExtension</i> is specified as DVD_SP_EXT_Caption_Big, the DVD Navigator tries to show U.S. English text in the "big caption" format in subpictures. If the default language or language extension is not found on a disc, the DVD Navigator selects the closest match.

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
 

 

