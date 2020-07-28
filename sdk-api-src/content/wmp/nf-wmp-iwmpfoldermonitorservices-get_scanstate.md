---
UID: NF:wmp.IWMPFolderMonitorServices.get_scanState
title: IWMPFolderMonitorServices::get_scanState (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_scanState method retrieves the scan state for the current scanning operation.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","get_scanState method","IWMPFolderMonitorServices.get_scanState","IWMPFolderMonitorServices::get_scanState","IWMPFolderMonitorServicesget_scanState","get_scanState","get_scanState method [Windows Media Player]","get_scanState method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_get_scanstate","wmp/IWMPFolderMonitorServices::get_scanState"]
old-location: wmp\iwmpfoldermonitorservices_get_scanstate.htm
tech.root: WMP
ms.assetid: 4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_scanState method, IWMPFolderMonitorServices.get_scanState, IWMPFolderMonitorServices::get_scanState, IWMPFolderMonitorServicesget_scanState, get_scanState, get_scanState method [Windows Media Player], get_scanState method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_scanstate, wmp/IWMPFolderMonitorServices::get_scanState
f1_keywords:
- wmp/IWMPFolderMonitorServices.get_scanState
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPFolderMonitorServices::get_scanState


## -description



This method and all other methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">IWMPEvents3::FolderScanStateChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan">IWMPFolderMonitorServices::startScan</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate">WMPFolderScanState</a>
 

 

