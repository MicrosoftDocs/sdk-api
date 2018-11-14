---
UID: NF:wmp.IWMPFolderMonitorServices.get_scannedFilesCount
title: IWMPFolderMonitorServices::get_scannedFilesCount
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_scannedFilesCount method retrieves the count of files inspected during the current scanning operation.
old-location: wmp\iwmpfoldermonitorservices_get_scannedfilescount.htm
tech.root: WMP
ms.assetid: 8b6a291b-b28d-4415-813c-5f4a5e1b2dca
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_scannedFilesCount method, IWMPFolderMonitorServices.get_scannedFilesCount, IWMPFolderMonitorServices::get_scannedFilesCount, IWMPFolderMonitorServicesget_scannedFilesCount, get_scannedFilesCount, get_scannedFilesCount method [Windows Media Player], get_scannedFilesCount method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_scannedfilescount, wmp/IWMPFolderMonitorServices::get_scannedFilesCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPFolderMonitorServices.get_scannedFilesCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPFolderMonitorServices.get_scannedFilesCount
: 
---

# IWMPFolderMonitorServices::get_scannedFilesCount


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices</a> interface are deprecated.

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




<a href="https://msdn.microsoft.com/07e9a49b-19a6-4ed2-b037-fe44ada920a1">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6">IWMPFolderMonitorServices::get_scanState</a>



<a href="https://msdn.microsoft.com/c54c5b7e-3abf-4006-a811-c80b06e6def9">IWMPFolderMonitorServices::startScan</a>



<a href="https://msdn.microsoft.com/20909420-5f90-4334-b21a-82d6cdc6d019">WMPFolderScanState</a>
 

 

