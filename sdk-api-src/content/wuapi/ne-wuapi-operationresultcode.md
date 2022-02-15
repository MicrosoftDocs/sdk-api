---
UID: NE:wuapi.tagOperationResultCode
title: OperationResultCode (wuapi.h)
description: Defines the possible results of a download, install, uninstall, or verification operation on an update.
helpviewer_keywords: ["OperationResultCode","OperationResultCode enumeration [Windows Update Agent]","orcAborted","orcFailed","orcInProgress","orcNotStarted","orcSucceeded","orcSucceededWithErrors","wua.operationresultcode","wuapi/OperationResultCode","wuapi/orcAborted","wuapi/orcFailed","wuapi/orcInProgress","wuapi/orcNotStarted","wuapi/orcSucceeded","wuapi/orcSucceededWithErrors"]
old-location: wua\operationresultcode.htm
tech.root: wua
ms.assetid: 02d3442e-d098-42b6-b1b1-cc2d1a815fa4
ms.date: 12/05/2018
ms.keywords: OperationResultCode, OperationResultCode enumeration [Windows Update Agent], orcAborted, orcFailed, orcInProgress, orcNotStarted, orcSucceeded, orcSucceededWithErrors, wua.operationresultcode, wuapi/OperationResultCode, wuapi/orcAborted, wuapi/orcFailed, wuapi/orcInProgress, wuapi/orcNotStarted, wuapi/orcSucceeded, wuapi/orcSucceededWithErrors
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OperationResultCode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOperationResultCode
 - wuapi/tagOperationResultCode
 - OperationResultCode
 - wuapi/OperationResultCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - OperationResultCode
---

# OperationResultCode enumeration


## -description

Defines the possible results of a download, install, uninstall, or verification operation on an update.

## -enum-fields

### -field orcNotStarted:0

The operation is not started.

### -field orcInProgress:1

The operation is in progress.

### -field orcSucceeded:2

The operation was completed successfully.

### -field orcSucceededWithErrors:3

The operation is complete, but one or more errors occurred during the operation. The results might be incomplete.

### -field orcFailed:4

The operation  failed to complete.

### -field orcAborted:5

The operation is canceled.

