---
UID: NF:wmp.IWMPControls3.getAudioLanguageID
title: IWMPControls3::getAudioLanguageID
author: windows-sdk-content
description: The getAudioLanguageID method retrieves the locale identifier (LCID) for a specified audio language index.
old-location: wmp\iwmpcontrols3_getaudiolanguageid.htm
tech.root: WMP
ms.assetid: 50874485-23fc-48cc-9149-7cbc3b8c0c00
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],getAudioLanguageID method, IWMPControls3.getAudioLanguageID, IWMPControls3::getAudioLanguageID, IWMPControls3getAudioLanguageID, getAudioLanguageID, getAudioLanguageID method [Windows Media Player], getAudioLanguageID method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_getaudiolanguageid, wmp/IWMPControls3::getAudioLanguageID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPControls3.getAudioLanguageID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::getAudioLanguageID


## -description



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




<a href="https://msdn.microsoft.com/en-us/library/Dd563183(v=VS.85).aspx">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563184(v=VS.85).aspx">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563186(v=VS.85).aspx">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563187(v=VS.85).aspx">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563188(v=VS.85).aspx">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563191(v=VS.85).aspx">IWMPControls3::put_currentAudioLanguage</a>
 

 

