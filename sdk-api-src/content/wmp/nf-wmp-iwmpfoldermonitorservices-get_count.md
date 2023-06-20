---
UID: NF:wmp.IWMPFolderMonitorServices.get_count
title: IWMPFolderMonitorServices::get_count (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_count method retrieves the count of monitored folders.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","get_count method","IWMPFolderMonitorServices.get_count","IWMPFolderMonitorServices::get_count","IWMPFolderMonitorServicesget_count","get_count","get_count method [Windows Media Player]","get_count method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_get_count","wmp/IWMPFolderMonitorServices::get_count"]
old-location: wmp\iwmpfoldermonitorservices_get_count.htm
tech.root: WMP
ms.assetid: cf80820a-d126-4af6-ba5e-c1188c5c00a4
ms.date: 4/26/2023
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_count method, IWMPFolderMonitorServices.get_count, IWMPFolderMonitorServices::get_count, IWMPFolderMonitorServicesget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_count, wmp/IWMPFolderMonitorServices::get_count
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
 - IWMPFolderMonitorServices::get_count
 - wmp/IWMPFolderMonitorServices::get_count
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
 - IWMPFolderMonitorServices.get_count
---

# IWMPFolderMonitorServices::get_count


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This method and all other methods of the <a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_count</b> method retrieves the count of monitored folders.

## -parameters

### -param plCount [out]

Pointer to a <b>long</b> that receives the count.

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

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>