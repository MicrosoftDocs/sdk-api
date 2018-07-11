---
UID: NF:wmp.IWMPFolderMonitorServices.get_count
title: IWMPFolderMonitorServices::get_count
author: windows-sdk-content
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The get_count method retrieves the count of monitored folders.
old-location: wmp\iwmpfoldermonitorservices_get_count.htm
old-project: WMP
ms.assetid: cf80820a-d126-4af6-ba5e-c1188c5c00a4
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],get_count method, IWMPFolderMonitorServices.get_count, IWMPFolderMonitorServices::get_count, IWMPFolderMonitorServicesget_count, get_count, get_count method [Windows Media Player], get_count method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_get_count, wmp/IWMPFolderMonitorServices::get_count
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPFolderMonitorServices.get_count
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPFolderMonitorServices::get_count


## -description



This method and all other methods of the <a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>get_count</b> method retrieves the count of monitored folders.




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



<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/42c3b03c-f8f8-4219-91e1-da54a175fb24">IWMPFolderMonitorServices Interface</a>
 

 

