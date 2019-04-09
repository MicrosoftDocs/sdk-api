---
UID: NF:wmp.IWMPFolderMonitorServices.startScan
title: IWMPFolderMonitorServices::startScan (wmp.h)
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The startScan method starts a scanning operation.
old-location: wmp\iwmpfoldermonitorservices_startscan.htm
tech.root: WMP
ms.assetid: c54c5b7e-3abf-4006-a811-c80b06e6def9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],startScan method, IWMPFolderMonitorServices.startScan, IWMPFolderMonitorServices::startScan, IWMPFolderMonitorServicesstartScan, startScan, startScan method [Windows Media Player], startScan method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_startscan, wmp/IWMPFolderMonitorServices::startScan
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
---

# IWMPFolderMonitorServices::startScan


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices</a> interface are deprecated.

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




<a href="https://msdn.microsoft.com/en-us/library/Dd563302(v=VS.85).aspx">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563373(v=VS.85).aspx">IWMPFolderMonitorServices::get_scanState</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563378(v=VS.85).aspx">IWMPFolderMonitorServices::stopScan</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564698(v=VS.85).aspx">WMPFolderScanState</a>
 

 

