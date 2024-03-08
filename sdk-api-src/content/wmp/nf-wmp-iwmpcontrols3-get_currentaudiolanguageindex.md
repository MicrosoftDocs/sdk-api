---
UID: NF:wmp.IWMPControls3.get_currentAudioLanguageIndex
title: IWMPControls3::get_currentAudioLanguageIndex (wmp.h)
description: The get_currentAudioLanguageIndex method retrieves the one-based index that corresponds to the audio language for playback.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","get_currentAudioLanguageIndex method","IWMPControls3.get_currentAudioLanguageIndex","IWMPControls3::get_currentAudioLanguageIndex","IWMPControls3get_currentAudioLanguageIndex","get_currentAudioLanguageIndex","get_currentAudioLanguageIndex method [Windows Media Player]","get_currentAudioLanguageIndex method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_get_currentaudiolanguageindex","wmp/IWMPControls3::get_currentAudioLanguageIndex"]
old-location: wmp\iwmpcontrols3_get_currentaudiolanguageindex.htm
tech.root: WMP
ms.assetid: 559ff3a8-b053-44f6-90dc-02f99614c51b
ms.date: 4/26/2023
ms.keywords: IWMPControls3 interface [Windows Media Player],get_currentAudioLanguageIndex method, IWMPControls3.get_currentAudioLanguageIndex, IWMPControls3::get_currentAudioLanguageIndex, IWMPControls3get_currentAudioLanguageIndex, get_currentAudioLanguageIndex, get_currentAudioLanguageIndex method [Windows Media Player], get_currentAudioLanguageIndex method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_currentaudiolanguageindex, wmp/IWMPControls3::get_currentAudioLanguageIndex
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
 - IWMPControls3::get_currentAudioLanguageIndex
 - wmp/IWMPControls3::get_currentAudioLanguageIndex
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
 - IWMPControls3.get_currentAudioLanguageIndex
---

# IWMPControls3::get_currentAudioLanguageIndex


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_currentAudioLanguageIndex</b> method retrieves the one-based index that corresponds to the audio language for playback.

## -parameters

### -param plIndex [out]

Pointer to a <b>long</b> containing the one-based index.

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

For Windows Media-based content, properties and methods related to language selection support only a single output.

Use the <b>get_audioLanguageCount</b> method to retrieve the number of supported audio languages.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">IWMPControls3::getAudioLanguageDescription</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguageid">IWMPControls3::getAudioLanguageID</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getlanguagename">IWMPControls3::getLanguageName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">IWMPControls3::get_audioLanguageCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">IWMPControls3::get_currentAudioLanguage</a>



<a href="/previous-versions/aa388723(v=vs.85)">IWMPControls3::put_currentAudioLanguageIndex</a>