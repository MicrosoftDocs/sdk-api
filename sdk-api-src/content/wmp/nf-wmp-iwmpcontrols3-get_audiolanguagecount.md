---
UID: NF:wmp.IWMPControls3.get_audioLanguageCount
title: IWMPControls3::get_audioLanguageCount (wmp.h)
description: The get_audioLanguageCount method retrieves the count of supported audio languages.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","get_audioLanguageCount method","IWMPControls3.get_audioLanguageCount","IWMPControls3::get_audioLanguageCount","IWMPControls3get_audioLanguageCount","get_audioLanguageCount","get_audioLanguageCount method [Windows Media Player]","get_audioLanguageCount method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_get_audiolanguagecount","wmp/IWMPControls3::get_audioLanguageCount"]
old-location: wmp\iwmpcontrols3_get_audiolanguagecount.htm
tech.root: WMP
ms.assetid: 7c714f97-4f6b-4a8b-904c-3ce0f8057533
ms.date: 4/26/2023
ms.keywords: IWMPControls3 interface [Windows Media Player],get_audioLanguageCount method, IWMPControls3.get_audioLanguageCount, IWMPControls3::get_audioLanguageCount, IWMPControls3get_audioLanguageCount, get_audioLanguageCount, get_audioLanguageCount method [Windows Media Player], get_audioLanguageCount method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_audiolanguagecount, wmp/IWMPControls3::get_audioLanguageCount
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
 - IWMPControls3::get_audioLanguageCount
 - wmp/IWMPControls3::get_audioLanguageCount
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
 - IWMPControls3.get_audioLanguageCount
---

# IWMPControls3::get_audioLanguageCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_audioLanguageCount</b> method retrieves the count of supported audio languages.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> containing the count.

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

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 1.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">IWMPControls3::getAudioLanguageDescription</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguageid">IWMPControls3::getAudioLanguageID</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getlanguagename">IWMPControls3::getLanguageName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">IWMPControls3::get_currentAudioLanguage</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">IWMPControls3::get_currentAudioLanguageIndex</a>