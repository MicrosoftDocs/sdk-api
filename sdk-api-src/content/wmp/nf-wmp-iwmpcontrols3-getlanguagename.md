---
UID: NF:wmp.IWMPControls3.getLanguageName
title: IWMPControls3::getLanguageName
author: windows-sdk-content
description: The getLanguageName method retrieves the name of the audio language with the specified locale identifier (LCID).
old-location: wmp\iwmpcontrols3_getlanguagename.htm
tech.root: WMP
ms.assetid: cbae09f6-be4d-4736-9e02-d5b85b82ae77
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],getLanguageName method, IWMPControls3.getLanguageName, IWMPControls3::getLanguageName, IWMPControls3getLanguageName, getLanguageName, getLanguageName method [Windows Media Player], getLanguageName method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_getlanguagename, wmp/IWMPControls3::getLanguageName
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
 - IWMPControls3.getLanguageName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::getLanguageName


## -description



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




<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/4530267c-8b43-4778-a396-f365f6dae5f3">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/50874485-23fc-48cc-9149-7cbc3b8c0c00">IWMPControls3::getAudioLanguageID</a>



<a href="https://msdn.microsoft.com/7c714f97-4f6b-4a8b-904c-3ce0f8057533">IWMPControls3::get_audioLanguageCount</a>



<a href="https://msdn.microsoft.com/6ea76479-950d-4bbf-a0e9-0e7b4ddecd52">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>



<a href="https://msdn.microsoft.com/7050ed77-f4bd-4c20-a661-fb0ea26af3a3">IWMPControls3::put_currentAudioLanguage</a>
 

 

