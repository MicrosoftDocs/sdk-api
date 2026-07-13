---
UID: NF:wia_xp.IWiaDataTransfer.idtGetExtendedTransferInfo
title: IWiaDataTransfer::idtGetExtendedTransferInfo (wia_xp.h)
description: The IWiaDataTransfer::idtGetExtendedTransferInfo retrieves extended information relating to data transfer buffers in the case of banded data transfers.
helpviewer_keywords: ["IWiaDataTransfer interface [WIA]","idtGetExtendedTransferInfo method","IWiaDataTransfer.idtGetExtendedTransferInfo","IWiaDataTransfer::idtGetExtendedTransferInfo","_wia_IWiaDataTransfer_idtGetExtendedTransferInfo","idtGetExtendedTransferInfo","idtGetExtendedTransferInfo method [WIA]","idtGetExtendedTransferInfo method [WIA]","IWiaDataTransfer interface","wia._wia_IWiaDataTransfer_idtGetExtendedTransferInfo","wia_xp/IWiaDataTransfer::idtGetExtendedTransferInfo"]
old-location: wia\_wia_IWiaDataTransfer_idtGetExtendedTransferInfo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtgetextendedtransferinfo.htm
ms.date: 12/05/2018
ms.keywords: IWiaDataTransfer interface [WIA],idtGetExtendedTransferInfo method, IWiaDataTransfer.idtGetExtendedTransferInfo, IWiaDataTransfer::idtGetExtendedTransferInfo, _wia_IWiaDataTransfer_idtGetExtendedTransferInfo, idtGetExtendedTransferInfo, idtGetExtendedTransferInfo method [WIA], idtGetExtendedTransferInfo method [WIA],IWiaDataTransfer interface, wia._wia_IWiaDataTransfer_idtGetExtendedTransferInfo, wia_xp/IWiaDataTransfer::idtGetExtendedTransferInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaDataTransfer::idtGetExtendedTransferInfo
 - wia_xp/IWiaDataTransfer::idtGetExtendedTransferInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDataTransfer.idtGetExtendedTransferInfo
archived: true
---

# IWiaDataTransfer::idtGetExtendedTransferInfo


## -description

The <b>IWiaDataTransfer::idtGetExtendedTransferInfo</b> retrieves extended information relating to data transfer buffers in the case of banded data transfers. Applications typically use this method to retrieve driver recommended settings for minimum buffer size, maximum buffer size, and optimal buffer size for banded data transfers.

## -parameters

### -param pExtendedTransferInfo [out]

Type: <b>PWIA_EXTENDED_TRANSFER_INFO</b>

Pointer to a <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_extended_transfer_info">WIA_EXTENDED_TRANSFER_INFO</a> structure containing the extended information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.