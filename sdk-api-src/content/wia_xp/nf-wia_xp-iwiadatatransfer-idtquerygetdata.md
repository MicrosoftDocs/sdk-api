---
UID: NF:wia_xp.IWiaDataTransfer.idtQueryGetData
title: IWiaDataTransfer::idtQueryGetData (wia_xp.h)
description: The IWiaDataTransfer::idtQueryGetData method is used by applications to query a Windows Image Acquisition (WIA) device to determine what types of data formats it supports.
helpviewer_keywords: ["IWiaDataTransfer interface [WIA]","idtQueryGetData method","IWiaDataTransfer.idtQueryGetData","IWiaDataTransfer::idtQueryGetData","_wia_IWiaDataTransfer_idtQueryGetData","idtQueryGetData","idtQueryGetData method [WIA]","idtQueryGetData method [WIA]","IWiaDataTransfer interface","wia._wia_IWiaDataTransfer_idtQueryGetData","wia_xp/IWiaDataTransfer::idtQueryGetData"]
old-location: wia\_wia_IWiaDataTransfer_idtQueryGetData.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtquerygetdata.htm
ms.date: 12/05/2018
ms.keywords: IWiaDataTransfer interface [WIA],idtQueryGetData method, IWiaDataTransfer.idtQueryGetData, IWiaDataTransfer::idtQueryGetData, _wia_IWiaDataTransfer_idtQueryGetData, idtQueryGetData, idtQueryGetData method [WIA], idtQueryGetData method [WIA],IWiaDataTransfer interface, wia._wia_IWiaDataTransfer_idtQueryGetData, wia_xp/IWiaDataTransfer::idtQueryGetData
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
 - IWiaDataTransfer::idtQueryGetData
 - wia_xp/IWiaDataTransfer::idtQueryGetData
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
 - IWiaDataTransfer.idtQueryGetData
archived: true
---

# IWiaDataTransfer::idtQueryGetData


## -description

The <b>IWiaDataTransfer::idtQueryGetData</b> method is used by applications to query a Windows Image Acquisition (WIA) device to determine what types of data formats it supports.

## -parameters

### -param pfe [in]

Type: <b><a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a>*</b>

Pointer to a <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise it returns a value specified in <a href="/windows/desktop/wia/-wia-error-codes">Error Codes</a>, or a standard COM error.

## -remarks

This method queries a device to determine the data formats it supports. Prior to a data transfer, an application can fill in the <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structure with the intended medium and data format information. It then calls <b>IWiaDataTransfer::idtQueryGetData</b> and receives a return value of S_OK if the data format and media type are supported by this device.