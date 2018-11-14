---
UID: NF:wmp.IWMPFolderMonitorServices.startScan
title: IWMPFolderMonitorServices::startScan
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The startScan method starts a scanning operation.
old-location: wmp\iwmpfoldermonitorservices_startscan.htm
tech.root: WMP
ms.assetid: c54c5b7e-3abf-4006-a811-c80b06e6def9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],startScan method, IWMPFolderMonitorServices.startScan, IWMPFolderMonitorServices::startScan, IWMPFolderMonitorServicesstartScan, startScan, startScan method [Windows Media Player], startScan method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_startscan, wmp/IWMPFolderMonitorServices::startScan
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
 - IWMPFolderMonitorServices.startScan
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
- IWMPFolderMonitorServices.startScan
: 
---

# IWMPFolderMonitorServices::startScan


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>startScan</b> method starts a scanning operation.




## -parameters






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




<a href="https://msdn.microsoft.com/07e9a49b-19a6-4ed2-b037-fe44ada920a1">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6">IWMPFolderMonitorServices::get_scanState</a>



<a href="https://msdn.microsoft.com/9b85cefb-3118-4e7f-b6f7-2f387057895e">IWMPFolderMonitorServices::stopScan</a>



<a href="https://msdn.microsoft.com/20909420-5f90-4334-b21a-82d6cdc6d019">WMPFolderScanState</a>
 

 

