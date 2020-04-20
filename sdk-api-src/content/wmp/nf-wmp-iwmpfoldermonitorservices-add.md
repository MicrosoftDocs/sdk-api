---
UID: NF:wmp.IWMPFolderMonitorServices.add
title: IWMPFolderMonitorServices::add (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The add method adds a folder to the list of monitored folders.helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","add method","IWMPFolderMonitorServices.add","IWMPFolderMonitorServices::add","IWMPFolderMonitorServicesadd","add","add method [Windows Media Player]","add method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_add","wmp/IWMPFolderMonitorServices::add"]
old-location: wmp\iwmpfoldermonitorservices_add.htm
tech.root: WMP
ms.assetid: f12bbc31-ce9d-4d0c-af1e-9078e7948eeb
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],add method, IWMPFolderMonitorServices.add, IWMPFolderMonitorServices::add, IWMPFolderMonitorServicesadd, add, add method [Windows Media Player], add method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_add, wmp/IWMPFolderMonitorServices::add
f1_keywords:
- wmp/IWMPFolderMonitorServices.add
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
- IWMPFolderMonitorServices.add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPFolderMonitorServices::add


## -description



This method and all other methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>add</b> method adds a folder to the list of monitored folders.




## -parameters




### -param bstrFolder [in]

<b>BSTR</b> containing the path to the folder.


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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove">IWMPFolderMonitorServices::remove</a>
 

 

