---
UID: NF:wmp.IWMPMedia.get_durationString
title: IWMPMedia::get_durationString (wmp.h)
description: The get_durationString method retrieves a string indicating the duration of the current media item in HH:MM:SS format.helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","get_durationString method","IWMPMedia.get_durationString","IWMPMedia2 interface [Windows Media Player]","get_durationString method","IWMPMedia2::get_durationString","IWMPMedia3 interface [Windows Media Player]","get_durationString method","IWMPMedia3::get_durationString","IWMPMedia::get_durationString","IWMPMediaget_durationString","get_durationString","get_durationString method [Windows Media Player]","get_durationString method [Windows Media Player]","IWMPMedia interface","get_durationString method [Windows Media Player]","IWMPMedia2 interface","get_durationString method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_get_durationstring","wmp/IWMPMedia2::get_durationString","wmp/IWMPMedia3::get_durationString","wmp/IWMPMedia::get_durationString"]
old-location: wmp\iwmpmedia_get_durationstring.htm
tech.root: WMP
ms.assetid: 540f4780-850f-41ec-940c-e8f7d3c96e6b
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_durationString method, IWMPMedia.get_durationString, IWMPMedia2 interface [Windows Media Player],get_durationString method, IWMPMedia2::get_durationString, IWMPMedia3 interface [Windows Media Player],get_durationString method, IWMPMedia3::get_durationString, IWMPMedia::get_durationString, IWMPMediaget_durationString, get_durationString, get_durationString method [Windows Media Player], get_durationString method [Windows Media Player],IWMPMedia interface, get_durationString method [Windows Media Player],IWMPMedia2 interface, get_durationString method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_durationstring, wmp/IWMPMedia2::get_durationString, wmp/IWMPMedia3::get_durationString, wmp/IWMPMedia::get_durationString
f1_keywords:
- wmp/IWMPMedia.get_durationString
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
- IWMPMedia.get_durationString
- IWMPMedia2.get_durationString
- IWMPMedia3.get_durationString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia::get_durationString


## -description



The <b>get_durationString</b> method retrieves a string indicating the duration of the current media item in HH:MM:SS format.




## -parameters




### -param pbstrDuration [out]

Pointer to a <b>BSTR</b> containing the duration.


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



If this method is used with a media item other than the one specified in <b>IWMPCore::get_currentMedia</b>, it may not contain a valid value. If the media item is less than an hour long, the hours portion of the return value is omitted.

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentmedia">IWMPCore::get_currentMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_duration">IWMPMedia::get_duration</a>
 

 

