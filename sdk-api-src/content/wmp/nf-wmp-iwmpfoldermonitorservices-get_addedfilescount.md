---
UID: NF:wmp.IWMPFolderMonitorServices.get_addedFilesCount
title: IWMPFolderMonitorServices::get_addedFilesCount
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_addedFilesCount method retrieves the count of files added to the library during the current scanning operation.
old-location: wmp\iwmpfoldermonitorservices_get_addedfilescount.htm
tech.root: WMP
ms.assetid: 56dcbb46-8de9-4fbe-b82c-927d42e39b2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_addedFilesCount method, IWMPFolderMonitorServices.get_addedFilesCount, IWMPFolderMonitorServices::get_addedFilesCount, IWMPFolderMonitorServicesget_addedFilesCount, get_addedFilesCount, get_addedFilesCount method [Windows Media Player], get_addedFilesCount method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_addedfilescount, wmp/IWMPFolderMonitorServices::get_addedFilesCount
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
 - IWMPFolderMonitorServices.get_addedFilesCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPFolderMonitorServices::get_addedFilesCount


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_addedFilesCount</b> method retrieves the count of files added to the library during the current scanning operation.




## -parameters




### -param plCount [out]

Pointer to a <b>long</b> that receives the file count.


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



A scanning operation consists of two phases: scanning and updating. The count of files added changes during the updating phase. You can determine the current scan state by calling <b>get_scanState</b> or by handling the <b>FolderScanStateChange</b> event.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563302(v=VS.85).aspx">IWMPEvents3::FolderScanStateChange</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563373(v=VS.85).aspx">IWMPFolderMonitorServices::get_scanState</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563377(v=VS.85).aspx">IWMPFolderMonitorServices::startScan</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564698(v=VS.85).aspx">WMPFolderScanState</a>
 

 

