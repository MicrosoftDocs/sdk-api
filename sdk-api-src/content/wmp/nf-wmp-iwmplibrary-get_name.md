---
UID: NF:wmp.IWMPLibrary.get_name
title: IWMPLibrary::get_name (wmp.h)
description: The get_name method retrieves the display name of the current library.
helpviewer_keywords: ["IWMPLibrary interface [Windows Media Player]","get_name method","IWMPLibrary.get_name","IWMPLibrary::get_name","IWMPLibraryget_name","get_name","get_name method [Windows Media Player]","get_name method [Windows Media Player]","IWMPLibrary interface","wmp.iwmplibrary_get_name","wmp/IWMPLibrary::get_name"]
old-location: wmp\iwmplibrary_get_name.htm
tech.root: WMP
ms.assetid: 28f1e3bc-3692-4fd0-a0b3-fecc3a173103
ms.date: 4/26/2023
ms.keywords: IWMPLibrary interface [Windows Media Player],get_name method, IWMPLibrary.get_name, IWMPLibrary::get_name, IWMPLibraryget_name, get_name, get_name method [Windows Media Player], get_name method [Windows Media Player],IWMPLibrary interface, wmp.iwmplibrary_get_name, wmp/IWMPLibrary::get_name
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
 - IWMPLibrary::get_name
 - wmp/IWMPLibrary::get_name
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
 - IWMPLibrary.get_name
---

# IWMPLibrary::get_name


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_name</b> method retrieves the display name of the current library.

## -parameters

### -param pbstrName [out]

Pointer to a string containing the name of the current library.

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



<a href="/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type">IWMPLibrary::get_type</a>