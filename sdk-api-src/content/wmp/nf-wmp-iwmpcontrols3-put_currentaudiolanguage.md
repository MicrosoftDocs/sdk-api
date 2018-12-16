---
UID: NF:wmp.IWMPControls3.put_currentAudioLanguage
title: IWMPControls3::put_currentAudioLanguage
author: windows-sdk-content
description: The put_currentAudioLanguage method specifies the locale identifier (LCID) of the audio language for playback.
old-location: wmp\iwmpcontrols3_put_currentaudiolanguage.htm
tech.root: WMP
ms.assetid: 7050ed77-f4bd-4c20-a661-fb0ea26af3a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],put_currentAudioLanguage method, IWMPControls3.put_currentAudioLanguage, IWMPControls3::put_currentAudioLanguage, IWMPControls3put_currentAudioLanguage, put_currentAudioLanguage, put_currentAudioLanguage method [Windows Media Player], put_currentAudioLanguage method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_put_currentaudiolanguage, wmp/IWMPControls3::put_currentAudioLanguage
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPControls3.put_currentAudioLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::put_currentAudioLanguage


## -description



The <b>put_currentAudioLanguage</b> method specifies the locale identifier (LCID) of the audio language for playback.




## -parameters




### -param lLangID [in]

<b>long</b> containing the LCID.


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

<b>Windows Media Player 10 Mobile: </b>This method only accepts a <b>long</b> set to 0 (the language-neutral LCID), otherwise an E_INVALIDARG <b>HRESULT</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563183(v=VS.85).aspx">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563184(v=VS.85).aspx">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563185(v=VS.85).aspx">IWMPControls3::getAudioLanguageID</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563186(v=VS.85).aspx">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563188(v=VS.85).aspx">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/f231ed72-e61d-4754-8ecb-e9a35f4abf2c">IWMPControls3::put_currentAudioLanguageIndex</a>
 

 

