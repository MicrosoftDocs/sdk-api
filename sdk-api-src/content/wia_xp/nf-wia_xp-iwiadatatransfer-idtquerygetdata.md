---
UID: NF:wia_xp.IWiaDataTransfer.idtQueryGetData
title: IWiaDataTransfer::idtQueryGetData method
author: windows-driver-content
description: The IWiaDataTransfer::idtQueryGetData method is used by applications to query a Windows Image Acquisition (WIA) device to determine what types of data formats it supports.
old-location: wia\_wia_IWiaDataTransfer_idtQueryGetData.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtquerygetdata.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IWiaDataTransfer, IWiaDataTransfer interface [WIA], idtQueryGetData method, IWiaDataTransfer::idtQueryGetData, _wia_IWiaDataTransfer_idtQueryGetData, idtQueryGetData method [WIA], idtQueryGetData method [WIA], IWiaDataTransfer interface, idtQueryGetData,IWiaDataTransfer.idtQueryGetData, wia._wia_IWiaDataTransfer_idtQueryGetData, wia_xp/IWiaDataTransfer::idtQueryGetData
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaservc.dll
api_name:
-	IWiaDataTransfer.idtQueryGetData
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDataTransfer::idtQueryGetData method


## -description


The <b>IWiaDataTransfer::idtQueryGetData</b> method is used by applications to query a Windows Image Acquisition (WIA) device to determine what types of data formats it supports.



## -parameters




### -param pfe [in]

Type: <b><a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise it returns a value specified in <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>, or a standard COM error.





## -remarks



This method queries a device to determine the data formats it supports. Prior to a data transfer, an application can fill in the <a href="https://msdn.microsoft.com/1dcc138b-b8c0-4d3a-bd9d-f4f5522d91ea">WIA_FORMAT_INFO</a> structure with the intended medium and data format information. It then calls <b>IWiaDataTransfer::idtQueryGetData</b> and receives a return value of S_OK if the data format and media type are supported by this device.



