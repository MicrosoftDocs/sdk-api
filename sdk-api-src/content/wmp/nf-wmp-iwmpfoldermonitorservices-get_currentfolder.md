---
UID: NF:wmp.IWMPFolderMonitorServices.get_currentFolder
title: IWMPFolderMonitorServices::get_currentFolder
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_currentFolder method retrieves the path of the folder currently being scanned.
old-location: wmp\iwmpfoldermonitorservices_get_currentfolder.htm
tech.root: WMP
ms.assetid: b0bc2f6a-c5ab-4dc5-a574-5b0fde16449a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_currentFolder method, IWMPFolderMonitorServices.get_currentFolder, IWMPFolderMonitorServices::get_currentFolder, IWMPFolderMonitorServicesget_currentFolder, get_currentFolder, get_currentFolder method [Windows Media Player], get_currentFolder method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_currentfolder, wmp/IWMPFolderMonitorServices::get_currentFolder
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
 - IWMPFolderMonitorServices.get_currentFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPFolderMonitorServices::get_currentFolder


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_currentFolder</b> method retrieves the path of the folder currently being scanned.




## -parameters




### -param pbstrFolder [out]

Pointer to a <b>BSTR</b> that receives the folder path string.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563366(v=VS.85).aspx">IWMPFolderMonitorServices Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563377(v=VS.85).aspx">IWMPFolderMonitorServices::startScan</a>
 

 

