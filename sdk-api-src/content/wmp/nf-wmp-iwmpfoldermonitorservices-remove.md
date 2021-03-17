---
UID: NF:wmp.IWMPFolderMonitorServices.remove
title: IWMPFolderMonitorServices::remove (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The remove method removes a folder from the list of monitored folders.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","remove method","IWMPFolderMonitorServices.remove","IWMPFolderMonitorServices::remove","IWMPFolderMonitorServicesremove","remove","remove method [Windows Media Player]","remove method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_remove","wmp/IWMPFolderMonitorServices::remove"]
old-location: wmp\iwmpfoldermonitorservices_remove.htm
tech.root: WMP
ms.assetid: 4f075c31-dd09-4d35-88fa-b93a373ad2d0
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],remove method, IWMPFolderMonitorServices.remove, IWMPFolderMonitorServices::remove, IWMPFolderMonitorServicesremove, remove, remove method [Windows Media Player], remove method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_remove, wmp/IWMPFolderMonitorServices::remove
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPFolderMonitorServices::remove
 - wmp/IWMPFolderMonitorServices::remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPFolderMonitorServices.remove
---

# IWMPFolderMonitorServices::remove


## -description

This method and all other methods of the <a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>remove</b> method removes a folder from the list of monitored folders.

## -parameters

### -param lIndex [in]

A <b>long</b> specifying the index of the folder to remove from the list.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add">IWMPFolderMonitorServices::add</a>