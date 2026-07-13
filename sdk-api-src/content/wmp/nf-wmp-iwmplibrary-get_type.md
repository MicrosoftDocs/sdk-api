---
UID: NF:wmp.IWMPLibrary.get_type
title: IWMPLibrary::get_type (wmp.h)
description: The get_type method retrieves a value that indicates the library type.
helpviewer_keywords: ["IWMPLibrary interface [Windows Media Player]","get_type method","IWMPLibrary.get_type","IWMPLibrary::get_type","IWMPLibraryget_type","get_type","get_type method [Windows Media Player]","get_type method [Windows Media Player]","IWMPLibrary interface","wmp.iwmplibrary_get_type","wmp/IWMPLibrary::get_type"]
old-location: wmp\iwmplibrary_get_type.htm
tech.root: WMP
ms.assetid: 95f36972-2227-4fe8-88d7-41f7aebbf67a
ms.date: 4/26/2023
ms.keywords: IWMPLibrary interface [Windows Media Player],get_type method, IWMPLibrary.get_type, IWMPLibrary::get_type, IWMPLibraryget_type, get_type, get_type method [Windows Media Player], get_type method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_type, wmp/IWMPLibrary::get_type
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
 - IWMPLibrary::get_type
 - wmp/IWMPLibrary::get_type
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
 - IWMPLibrary.get_type
---

# IWMPLibrary::get_type


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_type</b> method retrieves a value that indicates the library type.

## -parameters

### -param pwmplt [out]

Pointer to a variable that receives a value from the <b>WMPLibraryType</b> enumeration that indicates the library type.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name">IWMPLibrary::get_name</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmplibrarytype">WMPLibraryType</a>