---
UID: NF:wmp.IWMPMediaCollection2.getByAttributeAndMediaType
title: IWMPMediaCollection2::getByAttributeAndMediaType (wmp.h)
description: The getByAttributeAndMediaType method retrieves a pointer to an IWMPPlaylist interface. This interface represents a playlist that contains media items that have a specified attribute and media type.
helpviewer_keywords: ["IWMPMediaCollection2 interface [Windows Media Player]","getByAttributeAndMediaType method","IWMPMediaCollection2.getByAttributeAndMediaType","IWMPMediaCollection2::getByAttributeAndMediaType","IWMPMediaCollection2getByAttributeAndMediaType","getByAttributeAndMediaType","getByAttributeAndMediaType method [Windows Media Player]","getByAttributeAndMediaType method [Windows Media Player]","IWMPMediaCollection2 interface","wmp.iwmpmediacollection2_getbyattributeandmediatype","wmp/IWMPMediaCollection2::getByAttributeAndMediaType"]
old-location: wmp\iwmpmediacollection2_getbyattributeandmediatype.htm
tech.root: WMP
ms.assetid: cf925189-1f68-499c-9c98-063a0367dd3c
ms.date: 4/26/2023
ms.keywords: IWMPMediaCollection2 interface [Windows Media Player],getByAttributeAndMediaType method, IWMPMediaCollection2.getByAttributeAndMediaType, IWMPMediaCollection2::getByAttributeAndMediaType, IWMPMediaCollection2getByAttributeAndMediaType, getByAttributeAndMediaType, getByAttributeAndMediaType method [Windows Media Player], getByAttributeAndMediaType method [Windows Media Player],IWMPMediaCollection2 interface, wmp.iwmpmediacollection2_getbyattributeandmediatype, wmp/IWMPMediaCollection2::getByAttributeAndMediaType
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPMediaCollection2::getByAttributeAndMediaType
 - wmp/IWMPMediaCollection2::getByAttributeAndMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMediaCollection2.getByAttributeAndMediaType
---

# IWMPMediaCollection2::getByAttributeAndMediaType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getByAttributeAndMediaType</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface. This interface represents a playlist that contains media items that have a specified attribute and media type.

## -parameters

### -param bstrAttribute [in]

String that contains the specified attribute.

### -param bstrValue [in]

String that contains the specified value for the attribute that is specified in <i>bstrAttribute</i>.

### -param bstrMediaType [in]

String that contains the specified media type.

### -param ppMediaItems [out]

Address of a variable that receives a pointer to an <b>IWMPPlaylist</b> interface for the retrieved playlist.

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

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2">IWMPMediaCollection2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>