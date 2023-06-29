---
UID: NF:wmp.IWMPFolderMonitorServices.get_scannedFilesCount
title: IWMPFolderMonitorServices::get_scannedFilesCount (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_scannedFilesCount method retrieves the count of files inspected during the current scanning operation.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","get_scannedFilesCount method","IWMPFolderMonitorServices.get_scannedFilesCount","IWMPFolderMonitorServices::get_scannedFilesCount","IWMPFolderMonitorServicesget_scannedFilesCount","get_scannedFilesCount","get_scannedFilesCount method [Windows Media Player]","get_scannedFilesCount method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_get_scannedfilescount","wmp/IWMPFolderMonitorServices::get_scannedFilesCount"]
old-location: wmp\iwmpfoldermonitorservices_get_scannedfilescount.htm
tech.root: WMP
ms.assetid: 8b6a291b-b28d-4415-813c-5f4a5e1b2dca
ms.date: 4/26/2023
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_scannedFilesCount method, IWMPFolderMonitorServices.get_scannedFilesCount, IWMPFolderMonitorServices::get_scannedFilesCount, IWMPFolderMonitorServicesget_scannedFilesCount, get_scannedFilesCount, get_scannedFilesCount method [Windows Media Player], get_scannedFilesCount method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_scannedfilescount, wmp/IWMPFolderMonitorServices::get_scannedFilesCount
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
 - IWMPFolderMonitorServices::get_scannedFilesCount
 - wmp/IWMPFolderMonitorServices::get_scannedFilesCount
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
 - IWMPFolderMonitorServices.get_scannedFilesCount
---

# IWMPFolderMonitorServices::get_scannedFilesCount


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This method and all other methods of the <a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_scannedFilesCount</b> method retrieves the count of files inspected during the current scanning operation.

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

A scanning operation consists of two phases: scanning and updating. The count of files inspected changes during the scanning phase. You can determine the current scan state by calling <b>get_scanState</b> or by handling the <b>FolderScanStateChange</b> event.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">IWMPEvents3::FolderScanStateChange</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate">IWMPFolderMonitorServices::get_scanState</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan">IWMPFolderMonitorServices::startScan</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate">WMPFolderScanState</a>