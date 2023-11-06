---
UID: NF:wmp.IWMPSettings2.requestMediaAccessRights
title: IWMPSettings2::requestMediaAccessRights (wmp.h)
description: The requestMediaAccessRights method requests a specified level of access to the library.
helpviewer_keywords: ["IWMPSettings2 interface [Windows Media Player]","requestMediaAccessRights method","IWMPSettings2.requestMediaAccessRights","IWMPSettings2::requestMediaAccessRights","IWMPSettings2requestMediaAccessRights","requestMediaAccessRights","requestMediaAccessRights method [Windows Media Player]","requestMediaAccessRights method [Windows Media Player]","IWMPSettings2 interface","wmp.iwmpsettings2_requestmediaaccessrights","wmp/IWMPSettings2::requestMediaAccessRights"]
old-location: wmp\iwmpsettings2_requestmediaaccessrights.htm
tech.root: WMP
ms.assetid: 925a4c0b-d613-4248-a341-bfc51d02cb85
ms.date: 4/26/2023
ms.keywords: IWMPSettings2 interface [Windows Media Player],requestMediaAccessRights method, IWMPSettings2.requestMediaAccessRights, IWMPSettings2::requestMediaAccessRights, IWMPSettings2requestMediaAccessRights, requestMediaAccessRights, requestMediaAccessRights method [Windows Media Player], requestMediaAccessRights method [Windows Media Player],IWMPSettings2 interface, wmp.iwmpsettings2_requestmediaaccessrights, wmp/IWMPSettings2::requestMediaAccessRights
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSettings2::requestMediaAccessRights
 - wmp/IWMPSettings2::requestMediaAccessRights
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
 - IWMPSettings2.requestMediaAccessRights
---

# IWMPSettings2::requestMediaAccessRights


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>requestMediaAccessRights</b> method requests a specified level of access to the library.

## -parameters

### -param bstrDesiredAccess [in]

<b>BSTR</b> containing the one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>none</td>
<td>Current item access rights only.</td>
</tr>
<tr>
<td>read</td>
<td>Read access rights only.</td>
</tr>
<tr>
<td>full</td>
<td>Read/Write access rights.</td>
</tr>
</table>

### -param pvbAccepted [out]

Pointer to a <b>VARIANT_BOOL</b> indicating whether the requested access rights were granted.

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

A webpage must first request permission from the user to read information from or write data to the library. Invoking this method prompts the user with a dialog box that requests the specified permission level. This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted. The current access rights level can be retrieved by using <b>IWMPSettings2::get_mediaAccessRights</b>.

Applications running on the user's computer are not required to use this method.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>VARIANT_BOOL</b> set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings2">IWMPSettings2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>