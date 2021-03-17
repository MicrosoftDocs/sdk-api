---
UID: NF:wmp.IWMPControls3.get_currentAudioLanguage
title: IWMPControls3::get_currentAudioLanguage (wmp.h)
description: The get_currentAudioLanguage method retrieves the locale identifier (LCID) of the audio language for playback.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","get_currentAudioLanguage method","IWMPControls3.get_currentAudioLanguage","IWMPControls3::get_currentAudioLanguage","IWMPControls3get_currentAudioLanguage","get_currentAudioLanguage","get_currentAudioLanguage method [Windows Media Player]","get_currentAudioLanguage method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_get_currentaudiolanguage","wmp/IWMPControls3::get_currentAudioLanguage"]
old-location: wmp\iwmpcontrols3_get_currentaudiolanguage.htm
tech.root: WMP
ms.assetid: 6ea76479-950d-4bbf-a0e9-0e7b4ddecd52
ms.date: 12/05/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],get_currentAudioLanguage method, IWMPControls3.get_currentAudioLanguage, IWMPControls3::get_currentAudioLanguage, IWMPControls3get_currentAudioLanguage, get_currentAudioLanguage, get_currentAudioLanguage method [Windows Media Player], get_currentAudioLanguage method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_currentaudiolanguage, wmp/IWMPControls3::get_currentAudioLanguage
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPControls3::get_currentAudioLanguage
 - wmp/IWMPControls3::get_currentAudioLanguage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPControls3.get_currentAudioLanguage
---

# IWMPControls3::get_currentAudioLanguage


## -description

The <b>get_currentAudioLanguage</b> method retrieves the locale identifier (LCID) of the audio language for playback.

## -parameters

### -param plLangID [out]

Pointer to a <b>long</b> containing the LCID.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

An LCID uniquely identifies a particular language dialect, called a locale.

For Windows Media-based content, properties and methods related to language selection support only a single output.

When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0 (the language-neutral LCID).

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">IWMPControls3::getAudioLanguageDescription</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguageid">IWMPControls3::getAudioLanguageID</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getlanguagename">IWMPControls3::getLanguageName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">IWMPControls3::get_audioLanguageCount</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentaudiolanguage">IWMPControls3::put_currentAudioLanguage</a>