---
UID: NN:wmp.IWMPControls3
title: IWMPControls3
author: windows-sdk-content
description: The IWMPControls3 interface provides methods that supplement the IWMPControls2 interface.
old-location: wmp\iwmpcontrols3.htm
old-project: WMP
ms.assetid: ee902912-4f09-4f61-9b81-f4bd50ace892
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPControls3, IWMPControls3 interface [Windows Media Player], IWMPControls3 interface [Windows Media Player],described, IWMPControls3Interface, wmp.iwmpcontrols3, wmp/IWMPControls3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPControls3
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPControls3 interface


## -description



The <b>IWMPControls3</b> interface provides methods that supplement the <b>IWMPControls2</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPControls3</b> interface inherits from <a href="https://msdn.microsoft.com/aadbd924-b583-4136-8d6c-e3c8c0b3872e">IWMPControls2</a>. <b>IWMPControls3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7c714f97-4f6b-4a8b-904c-3ce0f8057533">get_audioLanguageCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of supported audio languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea76479-950d-4bbf-a0e9-0e7b4ddecd52">get_currentAudioLanguage</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/559ff3a8-b053-44f6-90dc-02f99614c51b">get_currentAudioLanguageIndex</a>
</td>
<td align="left" width="63%">
Retrieves the one-based index that corresponds to the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbf981d7-1787-462c-b0d2-fd705f07ee23">get_currentPositionTimecode</a>
</td>
<td align="left" width="63%">
Retrieves the current position in the current media using a time code format. This property supports SMPTE time code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4530267c-8b43-4778-a396-f365f6dae5f3">getAudioLanguageDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description for the audio language corresponding to the specified one-based index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50874485-23fc-48cc-9149-7cbc3b8c0c00">getAudioLanguageID</a>
</td>
<td align="left" width="63%">
Retrieves the LCID for a specified audio language index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbae09f6-be4d-4736-9e02-d5b85b82ae77">getLanguageName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the audio language with the specified LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7050ed77-f4bd-4c20-a661-fb0ea26af3a3">put_currentAudioLanguage</a>
</td>
<td align="left" width="63%">
Specifies the LCID of the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f231ed72-e61d-4754-8ecb-e9a35f4abf2c">put_currentAudioLanguageIndex</a>
</td>
<td align="left" width="63%">
Specifies the one-based index that corresponds to the audio language for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35e32043-e613-4f23-b5ce-03bfe648a4c9">put_currentPositionTimecode</a>
</td>
<td align="left" width="63%">
Specifies the current position in the current media using SMPTE time code format.

</td>
</tr>
</table> 


Retrieve a pointer to an <b>IWMPControls3</b> interface by calling the <b>QueryInterface</b> method of an <a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls</a> interface.
	


## -see-also




<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/aadbd924-b583-4136-8d6c-e3c8c0b3872e">IWMPControls2 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

