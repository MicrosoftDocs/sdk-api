---
UID: NF:wmp.IWMPFolderMonitorServices.get_updateProgress
title: IWMPFolderMonitorServices::get_updateProgress (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_updateProgress method retrieves the update progress as percent complete.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","get_updateProgress method","IWMPFolderMonitorServices.get_updateProgress","IWMPFolderMonitorServices::get_updateProgress","IWMPFolderMonitorServicesget_updateProgress","get_updateProgress","get_updateProgress method [Windows Media Player]","get_updateProgress method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_get_updateprogress","wmp/IWMPFolderMonitorServices::get_updateProgress"]
old-location: wmp\iwmpfoldermonitorservices_get_updateprogress.htm
tech.root: WMP
ms.assetid: 60a612d2-8675-456f-b428-ddfd0b73fd83
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_updateProgress method, IWMPFolderMonitorServices.get_updateProgress, IWMPFolderMonitorServices::get_updateProgress, IWMPFolderMonitorServicesget_updateProgress, get_updateProgress, get_updateProgress method [Windows Media Player], get_updateProgress method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_updateprogress, wmp/IWMPFolderMonitorServices::get_updateProgress
f1_keywords:
- wmp/IWMPFolderMonitorServices.get_updateProgress
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
- IWMPFolderMonitorServices.get_updateProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPFolderMonitorServices::get_updateProgress


## -description



This method and all other methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_updateProgress</b> method retrieves the update progress as percent complete.




## -parameters




### -param plProgress [out]

Pointer to a <b>long</b> that indicates the progress as percent complete. Values range from 0 to 100.


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



A scanning operation consists of two phases: scanning and updating. This method indicates progress of the second phase. You can determine the current scan state by calling <b>get_scanState</b> or by handling the <b>FolderScanStateChange</b> event.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">IWMPEvents3::FolderScanStateChange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate">IWMPFolderMonitorServices::get_scanState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan">IWMPFolderMonitorServices::startScan</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate">WMPFolderScanState</a>
 

 

