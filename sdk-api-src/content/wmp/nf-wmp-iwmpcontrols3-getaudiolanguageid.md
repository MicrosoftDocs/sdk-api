---
UID: NF:wmp.IWMPControls3.getAudioLanguageID
title: IWMPControls3::getAudioLanguageID (wmp.h)
description: The getAudioLanguageID method retrieves the locale identifier (LCID) for a specified audio language index.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","getAudioLanguageID method","IWMPControls3.getAudioLanguageID","IWMPControls3::getAudioLanguageID","IWMPControls3getAudioLanguageID","getAudioLanguageID","getAudioLanguageID method [Windows Media Player]","getAudioLanguageID method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_getaudiolanguageid","wmp/IWMPControls3::getAudioLanguageID"]
old-location: wmp\iwmpcontrols3_getaudiolanguageid.htm
tech.root: WMP
ms.assetid: 50874485-23fc-48cc-9149-7cbc3b8c0c00
ms.date: 4/26/2023
ms.keywords: IWMPControls3 interface [Windows Media Player],getAudioLanguageID method, IWMPControls3.getAudioLanguageID, IWMPControls3::getAudioLanguageID, IWMPControls3getAudioLanguageID, getAudioLanguageID, getAudioLanguageID method [Windows Media Player], getAudioLanguageID method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_getaudiolanguageid, wmp/IWMPControls3::getAudioLanguageID
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
 - IWMPControls3::getAudioLanguageID
 - wmp/IWMPControls3::getAudioLanguageID
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
 - IWMPControls3.getAudioLanguageID
---

# IWMPControls3::getAudioLanguageID


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getAudioLanguageID</b> method retrieves the locale identifier (LCID) for a specified audio language index.

## -parameters

### -param lIndex [in]

<b>long</b> specifying the one-based index of the audio language.

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

Use the <b>get_audioLanguageCount</b> method to retrieve the number of supported audio languages, and then access an audio language individually by using a one-based index.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0 (the language-neutral LCID).

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">IWMPControls3::getAudioLanguageDescription</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getlanguagename">IWMPControls3::getLanguageName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">IWMPControls3::get_audioLanguageCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">IWMPControls3::get_currentAudioLanguage</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentaudiolanguage">IWMPControls3::put_currentAudioLanguage</a>