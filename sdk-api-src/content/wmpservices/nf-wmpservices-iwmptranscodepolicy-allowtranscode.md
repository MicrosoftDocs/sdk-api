---
UID: NF:wmpservices.IWMPTranscodePolicy.allowTranscode
title: IWMPTranscodePolicy::allowTranscode (wmpservices.h)
description: The allowTranscode method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.
helpviewer_keywords: ["IWMPTranscodePolicy interface [Windows Media Player]","allowTranscode method","IWMPTranscodePolicy.allowTranscode","IWMPTranscodePolicy::allowTranscode","IWMPTranscodePolicyallowTranscode","allowTranscode","allowTranscode method [Windows Media Player]","allowTranscode method [Windows Media Player]","IWMPTranscodePolicy interface","wmp.iwmptranscodepolicy_allowtranscode","wmpservices/IWMPTranscodePolicy::allowTranscode"]
old-location: wmp\iwmptranscodepolicy_allowtranscode.htm
tech.root: WMP
ms.assetid: 6b43e247-cbb5-4ef1-8906-5ce7e1e58484
ms.date: 4/26/2023
ms.keywords: IWMPTranscodePolicy interface [Windows Media Player],allowTranscode method, IWMPTranscodePolicy.allowTranscode, IWMPTranscodePolicy::allowTranscode, IWMPTranscodePolicyallowTranscode, allowTranscode, allowTranscode method [Windows Media Player], allowTranscode method [Windows Media Player],IWMPTranscodePolicy interface, wmp.iwmptranscodepolicy_allowtranscode, wmpservices/IWMPTranscodePolicy::allowTranscode
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
 - IWMPTranscodePolicy::allowTranscode
 - wmpservices/IWMPTranscodePolicy::allowTranscode
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
 - IWMPTranscodePolicy.allowTranscode
---

# IWMPTranscodePolicy::allowTranscode


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>allowTranscode</b> method retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to the Windows Media format.

## -parameters

### -param pvbAllow [out]

Pointer to a <b>VARIANT_BOOL</b> that contains a value indicating whether transcoding is permitted.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

When you copy to a device a digital media file that is in a custom format, you must change the format of the content if the device does not support the custom format. This process is called transcoding.

If the format used by a digital media file is not supported, Windows Media Player first checks the registry for existing permission to transcode, as described in <a href="/windows/desktop/WMP/file-name-extension-registry-settings">File Name Extension Registry Settings</a>. If the custom format type is registered for permission to transcode, Windows Media Player locates the DirectShow source filter for the custom format type and calls <b>QueryInterface</b> to retrieve a pointer to <b>IWMPTranscodePolicy</b>. If the interface pointer is retrieved, the Player calls <b>IWMPTranscodePolicy::allowTranscode</b>. If <b>allowTranscode</b> returns VARIANT_TRUE, Windows Media Player performs the necessary transcoding. Otherwise, Windows Media Player does not copy the digital media file to the device. If any filter in the DirectShow graph returns VARIANT_FALSE from <b>allowTranscode</b>, the transcoding operation will fail.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy">IWMPTranscodePolicy Interface</a>