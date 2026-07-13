---
UID: NF:wmp.IWMPClosedCaption.put_SAMIFileName
title: IWMPClosedCaption::put_SAMIFileName (wmp.h)
description: The put_SAMIFileName method specifies the name of the file containing the information needed for closed captioning.
helpviewer_keywords: ["IWMPClosedCaption interface [Windows Media Player]","put_SAMIFileName method","IWMPClosedCaption.put_SAMIFileName","IWMPClosedCaption::put_SAMIFileName","IWMPClosedCaptionput_SAMIFileName","put_SAMIFileName","put_SAMIFileName method [Windows Media Player]","put_SAMIFileName method [Windows Media Player]","IWMPClosedCaption interface","wmp.iwmpclosedcaption_put_samifilename","wmp/IWMPClosedCaption::put_SAMIFileName"]
old-location: wmp\iwmpclosedcaption_put_samifilename.htm
tech.root: WMP
ms.assetid: ebc05983-3375-4ace-b192-f427b9685310
ms.date: 4/26/2023
ms.keywords: IWMPClosedCaption interface [Windows Media Player],put_SAMIFileName method, IWMPClosedCaption.put_SAMIFileName, IWMPClosedCaption::put_SAMIFileName, IWMPClosedCaptionput_SAMIFileName, put_SAMIFileName, put_SAMIFileName method [Windows Media Player], put_SAMIFileName method [Windows Media Player],IWMPClosedCaption interface, wmp.iwmpclosedcaption_put_samifilename, wmp/IWMPClosedCaption::put_SAMIFileName
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
 - IWMPClosedCaption::put_SAMIFileName
 - wmp/IWMPClosedCaption::put_SAMIFileName
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
 - IWMPClosedCaption.put_SAMIFileName
---

# IWMPClosedCaption::put_SAMIFileName


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_SAMIFileName</b> method specifies the name of the file containing the information needed for closed captioning.

## -parameters

### -param bstrSAMIFileName [in]

<b>BSTR</b> containing the SAMI file name.

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

Once you specify a value using <b>put_SAMIFileName</b>, that value persists until you specify a new value (or until a new media item is opened by using the <i>sami</i> URL parameter). Therefore, you must specify a new value with this method before you play each new media item. The new value will take effect when the next media item is opened (or when <b>IWMPCore::close</b> is called). Specifying a new value by using <b>put_SAMIFileName</b> has no effect on the current media item.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption-get_samifilename">IWMPClosedCaption::get_SAMIFileName</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcore-close">IWMPCore::close</a>