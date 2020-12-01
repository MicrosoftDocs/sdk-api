---
UID: NF:wdsclientapi.WdsCliCancelTransfer
title: WdsCliCancelTransfer function (wdsclientapi.h)
description: Cancels a WDS transfer operation.
helpviewer_keywords: ["WdsCliCancelTransfer","WdsCliCancelTransfer function [Windows Deployment Services]","wds.wdsclicanceltransfer","wdsclientapi/WdsCliCancelTransfer"]
old-location: wds\wdsclicanceltransfer.htm
tech.root: wds
ms.assetid: 8d138b95-4be1-4f53-ac15-21503408954b
ms.date: 12/05/2018
ms.keywords: WdsCliCancelTransfer, WdsCliCancelTransfer function [Windows Deployment Services], wds.wdsclicanceltransfer, wdsclientapi/WdsCliCancelTransfer
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliCancelTransfer
 - wdsclientapi/WdsCliCancelTransfer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliCancelTransfer
---

# WdsCliCancelTransfer function


## -description

Cancels a WDS transfer operation.

## -parameters

### -param hTransfer [in]

A handle for the WDS transfer operation being canceled. This can be the handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferimage">WdsCliTransferImage</a> or <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferfile">WdsCliTransferFile</a> functions.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This function can be called from a callback function.