---
UID: NF:wmp.IWMPCdrom.eject
title: IWMPCdrom::eject (wmp.h)
description: The eject method ejects the CD or DVD from the drive.
helpviewer_keywords: ["IWMPCdrom interface [Windows Media Player]","eject method","IWMPCdrom.eject","IWMPCdrom::eject","IWMPCdromeject","eject","eject method [Windows Media Player]","eject method [Windows Media Player]","IWMPCdrom interface","wmp.iwmpcdrom_eject","wmp/IWMPCdrom::eject"]
old-location: wmp\iwmpcdrom_eject.htm
tech.root: WMP
ms.assetid: 1b17c405-0887-4948-b375-c1ebcf2a72b3
ms.date: 4/26/2023
ms.keywords: IWMPCdrom interface [Windows Media Player],eject method, IWMPCdrom.eject, IWMPCdrom::eject, IWMPCdromeject, eject, eject method [Windows Media Player], eject method [Windows Media Player],IWMPCdrom interface, wmp.iwmpcdrom_eject, wmp/IWMPCdrom::eject
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
 - IWMPCdrom::eject
 - wmp/IWMPCdrom::eject
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
 - IWMPCdrom.eject
---

# IWMPCdrom::eject


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>eject</b> method ejects the CD or DVD from the drive.



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

If the drive door is open, this method closes the door.

To use this method, read access to the library is required. For more information, see <a href="/windows/desktop/WMP/library-access">Library Access</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdrom">IWMPCdromInterface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_playstate">IWMPCore::get_playState</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-get_mediaaccessrights">IWMPSettings2::get_mediaAccessRights</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings2-requestmediaaccessrights">IWMPSettings2::requestMediaAccessRights</a>
