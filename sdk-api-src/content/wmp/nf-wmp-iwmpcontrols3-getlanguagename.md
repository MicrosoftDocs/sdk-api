---
UID: NF:wmp.IWMPControls3.getLanguageName
title: IWMPControls3::getLanguageName (wmp.h)
description: The getLanguageName method retrieves the name of the audio language with the specified locale identifier (LCID).
helpviewer_keywords: ["IWMPControls3 interface [Windows Media Player]","getLanguageName method","IWMPControls3.getLanguageName","IWMPControls3::getLanguageName","IWMPControls3getLanguageName","getLanguageName","getLanguageName method [Windows Media Player]","getLanguageName method [Windows Media Player]","IWMPControls3 interface","wmp.iwmpcontrols3_getlanguagename","wmp/IWMPControls3::getLanguageName"]
old-location: wmp\iwmpcontrols3_getlanguagename.htm
tech.root: WMP
ms.assetid: cbae09f6-be4d-4736-9e02-d5b85b82ae77
ms.date: 4/26/2023
ms.keywords: IWMPControls3 interface [Windows Media Player],getLanguageName method, IWMPControls3.getLanguageName, IWMPControls3::getLanguageName, IWMPControls3getLanguageName, getLanguageName, getLanguageName method [Windows Media Player], getLanguageName method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_getlanguagename, wmp/IWMPControls3::getLanguageName
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
 - IWMPControls3::getLanguageName
 - wmp/IWMPControls3::getLanguageName
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
 - IWMPControls3.getLanguageName
---

# IWMPControls3::getLanguageName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getLanguageName</b> method retrieves the name of the audio language with the specified locale identifier (LCID).

## -parameters

### -param lLangID [in]

<b>long</b> specifying the LCID.

### -param pbstrLangName [out]

Pointer to a <b>BSTR</b> containing the audio language name.

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

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3">IWMPControls3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">IWMPControls3::getAudioLanguageDescription</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguageid">IWMPControls3::getAudioLanguageID</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">IWMPControls3::get_audioLanguageCount</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">IWMPControls3::get_currentAudioLanguage</a>



<a href="/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentaudiolanguage">IWMPControls3::put_currentAudioLanguage</a>