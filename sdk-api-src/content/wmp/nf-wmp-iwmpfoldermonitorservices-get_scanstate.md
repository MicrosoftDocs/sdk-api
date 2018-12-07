---
UID: NF:wmp.IWMPFolderMonitorServices.get_scanState
title: IWMPFolderMonitorServices::get_scanState
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_scanState method retrieves the scan state for the current scanning operation.
old-location: wmp\iwmpfoldermonitorservices_get_scanstate.htm
tech.root: WMP
ms.assetid: 4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_scanState method, IWMPFolderMonitorServices.get_scanState, IWMPFolderMonitorServices::get_scanState, IWMPFolderMonitorServicesget_scanState, get_scanState, get_scanState method [Windows Media Player], get_scanState method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_scanstate, wmp/IWMPFolderMonitorServices::get_scanState
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
 - IWMPFolderMonitorServices.get_scanState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPFolderMonitorServices::get_scanState


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_scanState</b> method retrieves the scan state for the current scanning operation.




## -parameters




### -param pwmpfss [out]

Pointer to a variable that receives a value from the <b>WMPFolderScanState</b> enumeration that indicates the scan state.


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



A scanning operation consists of two phases: scanning and updating. During the first phase, Windows Media Player determines which digital media files to add to the library. During the second phase, the Player adds the files. You can handle the <b>FolderScanStateChange</b> event to receive notifications when the scan state changes.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/07e9a49b-19a6-4ed2-b037-fe44ada920a1">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/c54c5b7e-3abf-4006-a811-c80b06e6def9">IWMPFolderMonitorServices::startScan</a>



<a href="https://msdn.microsoft.com/20909420-5f90-4334-b21a-82d6cdc6d019">WMPFolderScanState</a>
 

 

