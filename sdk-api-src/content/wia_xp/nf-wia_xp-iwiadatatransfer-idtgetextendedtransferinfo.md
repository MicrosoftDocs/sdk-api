---
UID: NF:wia_xp.IWiaDataTransfer.idtGetExtendedTransferInfo
title: IWiaDataTransfer::idtGetExtendedTransferInfo
author: windows-sdk-content
description: The IWiaDataTransfer::idtGetExtendedTransferInfo retrieves extended information relating to data transfer buffers in the case of banded data transfers.
old-location: wia\_wia_IWiaDataTransfer_idtGetExtendedTransferInfo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtgetextendedtransferinfo.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWiaDataTransfer interface [WIA],idtGetExtendedTransferInfo method, IWiaDataTransfer.idtGetExtendedTransferInfo, IWiaDataTransfer::idtGetExtendedTransferInfo, _wia_IWiaDataTransfer_idtGetExtendedTransferInfo, idtGetExtendedTransferInfo, idtGetExtendedTransferInfo method [WIA], idtGetExtendedTransferInfo method [WIA],IWiaDataTransfer interface, wia._wia_IWiaDataTransfer_idtGetExtendedTransferInfo, wia_xp/IWiaDataTransfer::idtGetExtendedTransferInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDataTransfer.idtGetExtendedTransferInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaDataTransfer::idtGetExtendedTransferInfo


## -description


The <b>IWiaDataTransfer::idtGetExtendedTransferInfo</b> retrieves extended information relating to data transfer buffers in the case of banded data transfers. Applications typically use this method to retrieve driver recommended settings for minimum buffer size, maximum buffer size, and optimal buffer size for banded data transfers. 



## -parameters




### -param pExtendedTransferInfo [out]

Type: <b>PWIA_EXTENDED_TRANSFER_INFO</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms629876(v=VS.85).aspx">WIA_EXTENDED_TRANSFER_INFO</a> structure containing the extended information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



