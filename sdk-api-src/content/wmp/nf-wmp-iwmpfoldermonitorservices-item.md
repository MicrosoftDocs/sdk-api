---
UID: NF:wmp.IWMPFolderMonitorServices.item
title: IWMPFolderMonitorServices::item (wmp.h)
description: This method and all other methods of the IWMPFolderMonitorServices interface are deprecated.The item method retrieves the path to the folder corresponding to the specified index.
helpviewer_keywords: ["IWMPFolderMonitorServices interface [Windows Media Player]","item method","IWMPFolderMonitorServices.item","IWMPFolderMonitorServices::item","IWMPFolderMonitorServicesitem","item","item method [Windows Media Player]","item method [Windows Media Player]","IWMPFolderMonitorServices interface","wmp.iwmpfoldermonitorservices_item","wmp/IWMPFolderMonitorServices::item"]
old-location: wmp\iwmpfoldermonitorservices_item.htm
tech.root: WMP
ms.assetid: d9c79b85-ac64-456c-95b2-fe28a8c99fac
ms.date: 4/26/2023
ms.keywords: IWMPFolderMonitorServices interface [Windows Media Player],item method, IWMPFolderMonitorServices.item, IWMPFolderMonitorServices::item, IWMPFolderMonitorServicesitem, item, item method [Windows Media Player], item method [Windows Media Player],IWMPFolderMonitorServices interface, wmp.iwmpfoldermonitorservices_item, wmp/IWMPFolderMonitorServices::item
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
 - IWMPFolderMonitorServices::item
 - wmp/IWMPFolderMonitorServices::item
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
 - IWMPFolderMonitorServices.item
---

# IWMPFolderMonitorServices::item


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

This method and all other methods of the <a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices</a> interface are deprecated.

The <b>item</b> method retrieves the path to the folder corresponding to the specified index.

## -parameters

### -param lIndex [in]

A <b>long</b> specifying the index of the folder to retrieve.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices">IWMPFolderMonitorServices Interface</a>