---
UID: NF:wmp.IWMPControls3.put_currentAudioLanguageIndex
title: IWMPControls3::put_currentAudioLanguageIndex (wmp.h)
description: The put_currentAudioLanguageIndex method specifies the one-based index that corresponds to the audio language for playback.
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","put_currentAudioLanguageIndex method","IWMPControls3.put_currentAudioLanguageIndex","IWMPControls3::put_currentAudioLanguageIndex","IWMPControls3put_currentAudioLanguageIndex","put_currentAudioLanguageIndex","put_currentAudioLanguageIndex method [Windows Media Player]","put_currentAudioLanguageIndex method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_put_currentaudiolanguageindex","wmp/IWMPControls3::put_currentAudioLanguageIndex"]
old-location: wmp\iwmpcontrols3_put_currentaudiolanguageindex.htm
tech.root: WMP
ms.assetid: f231ed72-e61d-4754-8ecb-e9a35f4abf2c
ms.date: 4/26/2023
ms.keywords: IWMPControls3 interface [Windows Media Player],put_currentAudioLanguageIndex method, IWMPControls3.put_currentAudioLanguageIndex, IWMPControls3::put_currentAudioLanguageIndex, IWMPControls3put_currentAudioLanguageIndex, put_currentAudioLanguageIndex, put_currentAudioLanguageIndex method [Windows Media Player], put_currentAudioLanguageIndex method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_put_currentaudiolanguageindex, wmp/IWMPControls3::put_currentAudioLanguageIndex
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
 - IWMPControls3::put_currentAudioLanguageIndex
 - wmp/IWMPControls3::put_currentAudioLanguageIndex
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
 - IWMPControls3.put_currentAudioLanguageIndex
---

# IWMPControls3::put_currentAudioLanguageIndex


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_currentAudioLanguageIndex</b> method specifies the one-based index that corresponds to the audio language for playback.

## -parameters

### -param lIndex [in]

<b>long</b> containing the one-based index.

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

<b>Windows Media Player 10 Mobile: </b>This method only accepts a <b>long</b> set to 0, otherwise an E_INVALIDARG <b>HRESULT</b> is returned.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">IWMPControls3::get_audioLanguageCount</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentaudiolanguage">IWMPControls3::put_currentAudioLanguage</a>