---
UID: NF:wmp.IWMPControls3.getAudioLanguageDescription
title: IWMPControls3::getAudioLanguageDescription (wmp.h)
author: windows-sdk-content
description: The getAudioLanguageDescription method retrieves the description for the audio language corresponding to the specified one-based index.
old-location: wmp\iwmpcontrols3_getaudiolanguagedescription.htm
tech.root: WMP
ms.assetid: 4530267c-8b43-4778-a396-f365f6dae5f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],getAudioLanguageDescription method, IWMPControls3.getAudioLanguageDescription, IWMPControls3::getAudioLanguageDescription, IWMPControls3getAudioLanguageDescription, getAudioLanguageDescription, getAudioLanguageDescription method [Windows Media Player], getAudioLanguageDescription method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_getaudiolanguagedescription, wmp/IWMPControls3::getAudioLanguageDescription
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
 - IWMPControls3.getAudioLanguageDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::getAudioLanguageDescription


## -description



The <b>getAudioLanguageDescription</b> method retrieves the description for the audio language corresponding to the specified one-based index.




## -parameters




### -param lIndex [in]

<b>long</b> specifying the one-based audio language index.


### -param pbstrLangDesc [out]

Pointer to a <b>BSTR</b> containing the description.


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

Use the <b>get_audioLanguageCount</b> method to retrieve the number of supported audio languages, and then access an audio language individually by using a one-based index.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563183(v=VS.85).aspx">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563185(v=VS.85).aspx">IWMPControls3::getAudioLanguageID</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563186(v=VS.85).aspx">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563187(v=VS.85).aspx">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563188(v=VS.85).aspx">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563191(v=VS.85).aspx">IWMPControls3::put_currentAudioLanguage</a>
 

 

