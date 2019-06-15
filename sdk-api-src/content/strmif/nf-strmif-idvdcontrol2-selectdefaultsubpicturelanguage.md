---
UID: NF:strmif.IDvdControl2.SelectDefaultSubpictureLanguage
title: IDvdControl2::SelectDefaultSubpictureLanguage (strmif.h)
author: windows-sdk-content
description: The SelectDefaultSubpictureLanguage method sets the default language for subpicture text.
old-location: dshow\idvdcontrol2_selectdefaultsubpicturelanguage.htm
tech.root: DirectShow
ms.assetid: f49698cd-cc83-4f05-991d-2b3bba77c33a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectDefaultSubpictureLanguage method, IDvdControl2.SelectDefaultSubpictureLanguage, IDvdControl2::SelectDefaultSubpictureLanguage, IDvdControl2SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage, SelectDefaultSubpictureLanguage method [DirectShow], SelectDefaultSubpictureLanguage method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectdefaultsubpicturelanguage, strmif/IDvdControl2::SelectDefaultSubpictureLanguage
ms.topic: method
f1_keywords: ["strmif/IDvdControl2.SelectDefaultSubpictureLanguage"]
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
 - IDvdControl2.SelectDefaultSubpictureLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::SelectDefaultSubpictureLanguage


## -description



The <code>SelectDefaultSubpictureLanguage</code> method sets the default language for subpicture text.




## -parameters




### -param Language [in]

Locale identifier that specifies the default language.


### -param subpictureExtension [in]


<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_subpicture_lang_ext">DVD_SUBPICTURE_LANG_EXT</a> enumeration that specifies the default subpicture extension.


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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter is not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



This method selects the default language and format to use for subpictures and menus when the disc is played. For example, if <i>Language</i> is specified as 0x409 for U.S. English and <i>subpictureExtension</i> is specified as DVD_SP_EXT_Caption_Big, the DVD Navigator tries to show U.S. English text in the "big caption" format in subpictures. If the default language or language extension is not found on a disc, the DVD Navigator selects the closest match.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>
 

 

