---
UID: NF:wmp.IWMPClosedCaption.get_SAMIFileName
title: IWMPClosedCaption::get_SAMIFileName (wmp.h)
description: The get_SAMIFileName method retrieves the name of the file containing the information needed for closed captioning.
helpviewer_keywords: ["IWMPClosedCaption interface [Windows Media Player]","get_SAMIFileName method","IWMPClosedCaption.get_SAMIFileName","IWMPClosedCaption::get_SAMIFileName","IWMPClosedCaptionget_SAMIFileName","get_SAMIFileName","get_SAMIFileName method [Windows Media Player]","get_SAMIFileName method [Windows Media Player]","IWMPClosedCaption interface","wmp.iwmpclosedcaption_get_samifilename","wmp/IWMPClosedCaption::get_SAMIFileName"]
old-location: wmp\iwmpclosedcaption_get_samifilename.htm
tech.root: WMP
ms.assetid: 2f09df76-3bfc-48ce-881f-c905656ecbbf
ms.date: 4/26/2023
ms.keywords: IWMPClosedCaption interface [Windows Media Player],get_SAMIFileName method, IWMPClosedCaption.get_SAMIFileName, IWMPClosedCaption::get_SAMIFileName, IWMPClosedCaptionget_SAMIFileName, get_SAMIFileName, get_SAMIFileName method [Windows Media Player], get_SAMIFileName method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_get_samifilename, wmp/IWMPClosedCaption::get_SAMIFileName
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
 - IWMPClosedCaption::get_SAMIFileName
 - wmp/IWMPClosedCaption::get_SAMIFileName
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
 - IWMPClosedCaption.get_SAMIFileName
---

# IWMPClosedCaption::get_SAMIFileName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_SAMIFileName</b> method retrieves the name of the file containing the information needed for closed captioning.

## -parameters

### -param pbstrSAMIFileName [out]

Pointer to a <b>BSTR</b> containing the name of the Synchronized Accessible Media Interchange (SAMI) file.

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

The SAMI file must use an .smi or .sami file name extension.

If you do not specify a value by using <b>IWMPClosedCaption::put_SAMIFileName</b>, the <b>get_SAMIFileName</b> method retrieves a <b>BSTR</b> containing the default file or URL associated with the current media item. This association can occur when a SAMI file is specified by using the <i>sami</i> URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension). If there is no default SAMI file associated with the current media, <b>get_SAMIFileName</b> retrieves an empty string ("").

If you want Windows Media Player to use the default SAMI file associated with a particular media item, call <b>IWMPClosedCaption::put_SAMIFileName</b> using an empty string ("") before you play the next media item.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>BSTR</b> containing an empty string.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-put_samifilename">IWMPClosedCaption::put_SAMIFileName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-close">IWMPCore::close</a>