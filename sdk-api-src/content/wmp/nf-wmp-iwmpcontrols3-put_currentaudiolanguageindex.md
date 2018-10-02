---
UID: NF:wmp.IWMPControls3.put_currentAudioLanguageIndex
title: IWMPControls3::put_currentAudioLanguageIndex
author: windows-sdk-content
description: The put_currentAudioLanguageIndex method specifies the one-based index that corresponds to the audio language for playback.
old-location: wmp\iwmpcontrols3_put_currentaudiolanguageindex.htm
tech.root: WMP
ms.assetid: f231ed72-e61d-4754-8ecb-e9a35f4abf2c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],put_currentAudioLanguageIndex method, IWMPControls3.put_currentAudioLanguageIndex, IWMPControls3::put_currentAudioLanguageIndex, IWMPControls3put_currentAudioLanguageIndex, put_currentAudioLanguageIndex, put_currentAudioLanguageIndex method [Windows Media Player], put_currentAudioLanguageIndex method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_put_currentaudiolanguageindex, wmp/IWMPControls3::put_currentAudioLanguageIndex
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
 - IWMPControls3.put_currentAudioLanguageIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::put_currentAudioLanguageIndex


## -description



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




<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/7c714f97-4f6b-4a8b-904c-3ce0f8057533">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="https://msdn.microsoft.com/7050ed77-f4bd-4c20-a661-fb0ea26af3a3">IWMPControls3::put_currentAudioLanguage</a>
 

 

