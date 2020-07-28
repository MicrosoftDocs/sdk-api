---
UID: NF:wmp.IWMPSettings2.get_defaultAudioLanguage
title: IWMPSettings2::get_defaultAudioLanguage (wmp.h)
description: The get_defaultAudioLanguage method retrieves the LCID of the default audio language specified in Windows Media Player.
helpviewer_keywords: ["IWMPSettings2 interface [Windows Media Player]","get_defaultAudioLanguage method","IWMPSettings2.get_defaultAudioLanguage","IWMPSettings2::get_defaultAudioLanguage","IWMPSettings2get_defaultAudioLanguage","get_defaultAudioLanguage","get_defaultAudioLanguage method [Windows Media Player]","get_defaultAudioLanguage method [Windows Media Player]","IWMPSettings2 interface","wmp.iwmpsettings2_get_defaultaudiolanguage","wmp/IWMPSettings2::get_defaultAudioLanguage"]
old-location: wmp\iwmpsettings2_get_defaultaudiolanguage.htm
tech.root: WMP
ms.assetid: 890154b7-0aa8-475f-afe9-9ce71997a656
ms.date: 12/05/2018
ms.keywords: IWMPSettings2 interface [Windows Media Player],get_defaultAudioLanguage method, IWMPSettings2.get_defaultAudioLanguage, IWMPSettings2::get_defaultAudioLanguage, IWMPSettings2get_defaultAudioLanguage, get_defaultAudioLanguage, get_defaultAudioLanguage method [Windows Media Player], get_defaultAudioLanguage method [Windows Media Player],IWMPSettings2 interface, wmp.iwmpsettings2_get_defaultaudiolanguage, wmp/IWMPSettings2::get_defaultAudioLanguage
f1_keywords:
- wmp/IWMPSettings2.get_defaultAudioLanguage
dev_langs:
- c++
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
- IWMPSettings2.get_defaultAudioLanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSettings2::get_defaultAudioLanguage


## -description



The <b>get_defaultAudioLanguage</b> method retrieves the LCID of the default audio language specified in Windows Media Player.




## -parameters




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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcontrols3-get_currentaudiolanguage">IWMPControls3::get_currentAudioLanguage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings2">IWMPSettings2 Interface</a>
 

 

