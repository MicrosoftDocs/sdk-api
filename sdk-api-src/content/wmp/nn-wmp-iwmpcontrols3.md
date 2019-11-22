---
UID: NN:wmp.IWMPControls3
title: IWMPControls3 (wmp.h)

description: The IWMPControls3 interface provides methods that supplement the IWMPControls2 interface.
old-location: wmp\iwmpcontrols3.htm
tech.root: WMP
ms.assetid: ee902912-4f09-4f61-9b81-f4bd50ace892

ms.date: 12/05/2018
ms.keywords: IWMPControls3, IWMPControls3 interface [Windows Media Player], IWMPControls3 interface [Windows Media Player],described, IWMPControls3Interface, wmp.iwmpcontrols3, wmp/IWMPControls3
ms.topic: interface
f1_keywords: 
 - "wmp/IWMPControls3"
dev_langs:
 - c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPControls3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPControls3 interface


## -description



The <b>IWMPControls3</b> interface provides methods that supplement the <b>IWMPControls2</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPControls3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2">IWMPControls2</a>. <b>IWMPControls3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPControls3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_audiolanguagecount">get_audioLanguageCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of supported audio languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">get_currentAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguageindex">get_currentAudioLanguageIndex</a>
</td>
<td align="left" width="63%">
Retrieves the one-based index that corresponds to the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentpositiontimecode">get_currentPositionTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the current media using a time code format. This property supports SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguagedescription">getAudioLanguageDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description for the audio language corresponding to the specified one-based index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getaudiolanguageid">getAudioLanguageID</a>
</td>
<td align="left" width="63%">
Retrieves the LCID for a specified audio language index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-getlanguagename">getLanguageName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the audio language with the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentaudiolanguage">put_currentAudioLanguage</a>
</td>
<td align="left" width="63%">
Specifies the LCID of the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/aa388723(v=vs.85)">put_currentAudioLanguageIndex</a>
</td>
<td align="left" width="63%">
Specifies the one-based index that corresponds to the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-put_currentpositiontimecode">put_currentPositionTimecode</a>
</td>
<td align="left" width="63%">
Specifies the current position in the current media using SMPTE time code format.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPControls3</b> interface by calling the <b>QueryInterface</b> method of an <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls</a> interface.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2">IWMPControls2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

