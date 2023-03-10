---
UID: NF:wdsclientapi.WdsCliGetImageHandleFromTransferHandle
title: WdsCliGetImageHandleFromTransferHandle function (wdsclientapi.h)
description: Returns an image handle from a completed transfer handle. The handle is to the local copy of the image that's been transferred from the server to the client.
helpviewer_keywords: ["WdsCliGetImageHandleFromTransferHandle","WdsCliGetImageHandleFromTransferHandle function [Windows Deployment Services]","wds.wdscligetimagehandlefromtransferhandle","wdsclientapi/WdsCliGetImageHandleFromTransferHandle"]
old-location: wds\wdscligetimagehandlefromtransferhandle.htm
tech.root: wds
ms.assetid: d2356f34-9ef8-4d7d-bb01-843d1aa1cbed
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageHandleFromTransferHandle, WdsCliGetImageHandleFromTransferHandle function [Windows Deployment Services], wds.wdscligetimagehandlefromtransferhandle, wdsclientapi/WdsCliGetImageHandleFromTransferHandle
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
 - WdsCliGetImageHandleFromTransferHandle
 - wdsclientapi/WdsCliGetImageHandleFromTransferHandle
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
 - WdsCliGetImageHandleFromTransferHandle
---

# WdsCliGetImageHandleFromTransferHandle function


## -description

Returns an image handle from a completed transfer handle.  The handle is to the local copy of the image that's been transferred from the server to the client.

## -parameters

### -param hTransfer

A WDS transfer handle that has completed the transfer. This can be the handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferimage">WdsCliTransferImage</a> or <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferfile">WdsCliTransferFile</a> functions.

### -param phImageHandle [out]

A pointer to a location that contains an image handle.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

If the transfer is not yet complete when this function is called, it will return an error code.

Use the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function to close the image handle returned by this function.