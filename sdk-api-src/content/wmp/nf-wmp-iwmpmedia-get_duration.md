---
UID: NF:wmp.IWMPMedia.get_duration
title: IWMPMedia::get_duration
author: windows-sdk-content
description: The get_duration method retrieves the duration in seconds of the current media item..
old-location: wmp\iwmpmedia_get_duration.htm
tech.root: WMP
ms.assetid: 40313888-faa0-499e-9133-dc437f5ad44f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPMedia interface [Windows Media Player],get_duration method, IWMPMedia.get_duration, IWMPMedia2 interface [Windows Media Player],get_duration method, IWMPMedia2::get_duration, IWMPMedia3 interface [Windows Media Player],get_duration method, IWMPMedia3::get_duration, IWMPMedia::get_duration, IWMPMediaget_duration, get_duration, get_duration method [Windows Media Player], get_duration method [Windows Media Player],IWMPMedia interface, get_duration method [Windows Media Player],IWMPMedia2 interface, get_duration method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_get_duration, wmp/IWMPMedia2::get_duration, wmp/IWMPMedia3::get_duration, wmp/IWMPMedia::get_duration
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
 - IWMPMedia.get_duration
 - IWMPMedia2.get_duration
 - IWMPMedia3.get_duration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPMedia.get_duration
: 
---

# IWMPMedia::get_duration


## -description



The <b>get_duration</b> method retrieves the duration in seconds of the current media item..




## -parameters




### -param pDuration [out]

Pointer to a <b>double</b> containing the duration.


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



If this method is used with a media item other than the one specified in <b>IWMPCore::get_currentMedia</b>, it may not contain a valid value.

To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen. You can verify this by handling the <b>IWMPEvents::OpenStateChange</b> event or by periodically checking the value of <b>IWMPCore::get_openState</b>.

For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f199336-0555-40de-8d27-780b05ef9510">IWMPCore::get_currentMedia</a>



<a href="https://msdn.microsoft.com/66c7e52a-d7b4-4c37-a863-fb42f5415c0a">IWMPCore::get_openState</a>



<a href="https://msdn.microsoft.com/6f228bc5-39a4-4bf8-a887-43ba13c1c414">IWMPEvents::OpenStateChange</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/540f4780-850f-41ec-940c-e8f7d3c96e6b">IWMPMedia::get_durationString</a>
 

 

