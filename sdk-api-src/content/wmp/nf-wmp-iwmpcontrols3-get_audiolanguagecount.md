---
UID: NF:wmp.IWMPControls3.get_audioLanguageCount
title: IWMPControls3::get_audioLanguageCount
author: windows-sdk-content
description: The get_audioLanguageCount method retrieves the count of supported audio languages.
old-location: wmp\iwmpcontrols3_get_audiolanguagecount.htm
tech.root: WMP
ms.assetid: 7c714f97-4f6b-4a8b-904c-3ce0f8057533
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPControls3 interface [Windows Media Player],get_audioLanguageCount method, IWMPControls3.get_audioLanguageCount, IWMPControls3::get_audioLanguageCount, IWMPControls3get_audioLanguageCount, get_audioLanguageCount, get_audioLanguageCount method [Windows Media Player], get_audioLanguageCount method [Windows Media Player],IWMPControls3 interface, wmp.iwmpcontrols3_get_audiolanguagecount, wmp/IWMPControls3::get_audioLanguageCount
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
 - IWMPControls3.get_audioLanguageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPControls3::get_audioLanguageCount


## -description



The <b>get_audioLanguageCount</b> method retrieves the count of supported audio languages.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> containing the count.


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

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 1.




## -see-also




<a href="https://msdn.microsoft.com/ee902912-4f09-4f61-9b81-f4bd50ace892">IWMPControls3 Interface</a>



<a href="https://msdn.microsoft.com/4530267c-8b43-4778-a396-f365f6dae5f3">IWMPControls3::getAudioLanguageDescription</a>



<a href="https://msdn.microsoft.com/50874485-23fc-48cc-9149-7cbc3b8c0c00">IWMPControls3::getAudioLanguageID</a>



<a href="https://msdn.microsoft.com/cbae09f6-be4d-4736-9e02-d5b85b82ae77">IWMPControls3::getLanguageName</a>



<a href="https://msdn.microsoft.com/6ea76479-950d-4bbf-a0e9-0e7b4ddecd52">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">IWMPControls3::get_currentAudioLanguageIndex</a>
 

 

