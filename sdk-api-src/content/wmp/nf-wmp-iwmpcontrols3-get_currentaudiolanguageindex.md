---
UID: NF:wmp.IWMPControls3.get_currentAudioLanguageIndex
title: IWMPControls3::get_currentAudioLanguageIndex
author: windows-sdk-content
description: The get_currentAudioLanguageIndex method retrieves the one-based index that corresponds to the audio language for playback.
old-location: wmp\iwmpcontrols3_get_currentaudiolanguageindex.htm
tech.root: WMP
ms.assetid: 559ff3a8-b053-44f6-90dc-02f99614c51b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],get_currentAudioLanguageIndex method, IWMPControls3.get_currentAudioLanguageIndex, IWMPControls3::get_currentAudioLanguageIndex, IWMPControls3get_currentAudioLanguageIndex, get_currentAudioLanguageIndex, get_currentAudioLanguageIndex method [Windows Media Player], get_currentAudioLanguageIndex method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_currentaudiolanguageindex, wmp/IWMPControls3::get_currentAudioLanguageIndex
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
 - IWMPControls3.get_currentAudioLanguageIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::get_currentAudioLanguageIndex


## -description



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




<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/4530267c-8b43-4778-a396-f365f6dae5f3">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/50874485-23fc-48cc-9149-7cbc3b8c0c00">IWMPControls3::getAudioLanguageID</a>



<a href="https://msdn.microsoft.com/cbae09f6-be4d-4736-9e02-d5b85b82ae77">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/7c714f97-4f6b-4a8b-904c-3ce0f8057533">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/6ea76479-950d-4bbf-a0e9-0e7b4ddecd52">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/f231ed72-e61d-4754-8ecb-e9a35f4abf2c">IWMPControls3::put_currentAudioLanguageIndex</a>
 

 

