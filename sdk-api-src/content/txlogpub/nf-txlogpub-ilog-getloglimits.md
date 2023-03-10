---
UID: NF:txlogpub.ILog.GetLogLimits
title: ILog::GetLogLimits (txlogpub.h)
description: Retrieves information about the current bounds of the log.
helpviewer_keywords: ["GetLogLimits","GetLogLimits method [COM]","GetLogLimits method [COM]","ILog interface","ILog interface [COM]","GetLogLimits method","ILog.GetLogLimits","ILog::GetLogLimits","_com_ilog_getloglimits","com.ilog_getloglimits","txlogpub/ILog::GetLogLimits"]
old-location: com\ilog_getloglimits.htm
tech.root: com
ms.assetid: 06238436-6807-4588-9af9-03eb4c12f4e1
ms.date: 12/05/2018
ms.keywords: GetLogLimits, GetLogLimits method [COM], GetLogLimits method [COM],ILog interface, ILog interface [COM],GetLogLimits method, ILog.GetLogLimits, ILog::GetLogLimits, _com_ilog_getloglimits, com.ilog_getloglimits, txlogpub/ILog::GetLogLimits
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILog::GetLogLimits
 - txlogpub/ILog::GetLogLimits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog.GetLogLimits
---

# ILog::GetLogLimits


## -description

Retrieves information about the current bounds of the log.

## -parameters

### -param plsnFirst [in, out]

A pointer to the LSN of the first record in the log. This parameter can be <b>NULL</b> if the LSN of the first record is not needed.

### -param plsnLast [in, out]

A pointer to the LSN of the last record in the log. This parameter can be <b>NULL</b> if the LSN of the last record is not needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The limits returned by this method may include records that have not yet been written to disk.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>