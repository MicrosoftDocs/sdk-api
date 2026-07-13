---
UID: NF:wmp.IWMPCdrom.get_driveSpecifier
title: IWMPCdrom::get_driveSpecifier (wmp.h)
description: The get_driveSpecifier method retrieves the CD or DVD drive letter.
helpviewer_keywords: ["IWMPCdrom interface [Windows Media Player]","get_driveSpecifier method","IWMPCdrom.get_driveSpecifier","IWMPCdrom::get_driveSpecifier","IWMPCdromget_driveSpecifier","get_driveSpecifier","get_driveSpecifier method [Windows Media Player]","get_driveSpecifier method [Windows Media Player]","IWMPCdrom interface","wmp.iwmpcdrom_get_drivespecifier","wmp/IWMPCdrom::get_driveSpecifier"]
old-location: wmp\iwmpcdrom_get_drivespecifier.htm
tech.root: WMP
ms.assetid: 0bc7766b-1e5d-4ed4-8016-aa1e8e0a7cc1
ms.date: 4/26/2023
ms.keywords: IWMPCdrom interface [Windows Media Player],get_driveSpecifier method, IWMPCdrom.get_driveSpecifier, IWMPCdrom::get_driveSpecifier, IWMPCdromget_driveSpecifier, get_driveSpecifier, get_driveSpecifier method [Windows Media Player], get_driveSpecifier method [Windows Media Player],IWMPCdrom interface, wmp.iwmpcdrom_get_drivespecifier, wmp/IWMPCdrom::get_driveSpecifier
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMPCdrom::get_driveSpecifier
 - wmp/IWMPCdrom::get_driveSpecifier
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
 - IWMPCdrom.get_driveSpecifier
---

# IWMPCdrom::get_driveSpecifier


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_driveSpecifier</b> method retrieves the CD or DVD drive letter.

## -parameters

### -param pbstrDrive [out]

Pointer to a <b>BSTR</b> containing the drive.

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

Typically, DVD drives can play CD media, but CD drives cannot play DVD media.

This method retrieves a drive letter for a zero-based drive index within the range retrieved using the <b>IWMPCdromCollection::get_count</b> method. The value retrieved takes the form <i>X</i>:, where <i>X</i> represents the drive letter.

To retrieve the value of this property, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdrom Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count">IWMPCdromCollection::get_count</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>