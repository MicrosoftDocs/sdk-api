---
UID: NF:wdsclientapi.WdsCliWaitForTransfer
title: WdsCliWaitForTransfer function (wdsclientapi.h)
description: Waits for an image or file transfer to complete.
helpviewer_keywords: ["WdsCliWaitForTransfer","WdsCliWaitForTransfer function [Windows Deployment Services]","wds.wdscliwaitfortransfer","wdsclientapi/WdsCliWaitForTransfer"]
old-location: wds\wdscliwaitfortransfer.htm
tech.root: wds
ms.assetid: 2328ce69-5a2d-4c4e-bf24-95a379fb7faa
ms.date: 12/05/2018
ms.keywords: WdsCliWaitForTransfer, WdsCliWaitForTransfer function [Windows Deployment Services], wds.wdscliwaitfortransfer, wdsclientapi/WdsCliWaitForTransfer
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
 - WdsCliWaitForTransfer
 - wdsclientapi/WdsCliWaitForTransfer
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
 - WdsCliWaitForTransfer
---

# WdsCliWaitForTransfer function


## -description

Waits for an image or file transfer to complete.

## -parameters

### -param hTransfer [in]

A WDS transfer handle for the transfer being canceled. This can be the handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferimage">WdsCliTransferImage</a> or <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferfile">WdsCliTransferFile</a> functions.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

Calling this function from a callback function is not recommended.