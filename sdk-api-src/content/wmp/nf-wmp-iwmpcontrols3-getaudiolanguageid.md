---
UID: NF:wmp.IWMPControls3.getAudioLanguageID
title: IWMPControls3::getAudioLanguageID method
author: windows-driver-content
description: The getAudioLanguageID method retrieves the locale identifier (LCID) for a specified audio language index.
old-location: wmp\iwmpcontrols3_getaudiolanguageid.htm
old-project: WMP
ms.assetid: 50874485-23fc-48cc-9149-7cbc3b8c0c00
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPControls3, IWMPControls3 interface [Windows Media Player], getAudioLanguageID method, IWMPControls3::getAudioLanguageID, IWMPControls3getAudioLanguageID, getAudioLanguageID method [Windows Media Player], getAudioLanguageID method [Windows Media Player], IWMPControls3 interface, getAudioLanguageID,IWMPControls3.getAudioLanguageID, wmp.iwmpcontrols3_getaudiolanguageid, wmp/IWMPControls3::getAudioLanguageID
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPControls3.getAudioLanguageID
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls3::getAudioLanguageID method


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




<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/4530267c-8b43-4778-a396-f365f6dae5f3">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/cbae09f6-be4d-4736-9e02-d5b85b82ae77">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/7c714f97-4f6b-4a8b-904c-3ce0f8057533">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/6ea76479-950d-4bbf-a0e9-0e7b4ddecd52">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="https://msdn.microsoft.com/7050ed77-f4bd-4c20-a661-fb0ea26af3a3">IWMPControls3::put_currentAudioLanguage</a>
 

 

