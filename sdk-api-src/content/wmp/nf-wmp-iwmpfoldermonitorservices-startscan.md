---
UID: NF:wmp.IWMPFolderMonitorServices.startScan
title: IWMPFolderMonitorServices::startScan (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The startScan method starts a scanning operation.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","startScan method","IWMPFolderMonitorServices.startScan","IWMPFolderMonitorServices::startScan","IWMPFolderMonitorServicesstartScan","startScan","startScan method [Windows Media Player]","startScan method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_startscan","wmp/IWMPFolderMonitorServices::startScan"]
old-location: wmp\iwmpfoldermonitorservices_startscan.htm
tech.root: WMP
ms.assetid: c54c5b7e-3abf-4006-a811-c80b06e6def9
ms.date: 4/26/2023
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],startScan method, IWMPFolderMonitorServices.startScan, IWMPFolderMonitorServices::startScan, IWMPFolderMonitorServicesstartScan, startScan, startScan method [Windows Media Player], startScan method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_startscan, wmp/IWMPFolderMonitorServices::startScan
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
 - IWMPFolderMonitorServices::startScan
 - wmp/IWMPFolderMonitorServices::startScan
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
 - IWMPFolderMonitorServices.startScan
---

# IWMPFolderMonitorServices::startScan


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This method and all other methods of the <a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>startScan</b> method starts a scanning operation.



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

The <b>startScan</b> method should always be paired with a call to the <b>stopScan</b> method. You should never call the <b>startScan</b> method twice in a row. A scanning operation consists of two phases: scanning and updating. You can determine the current scan state by calling <b>get_scanState</b> or by handling the <b>FolderScanStateChange</b> event.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">IWMPEvents3::FolderScanStateChange</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate">IWMPFolderMonitorServices::get_scanState</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan">IWMPFolderMonitorServices::stopScan</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate">WMPFolderScanState</a>
