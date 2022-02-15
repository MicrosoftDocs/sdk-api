---
UID: NF:shdeprecated.ITravelLog.Clone
title: ITravelLog::Clone (shdeprecated.h)
description: Deprecated. Duplicates the contents of the current travel log.
helpviewer_keywords: ["Clone","Clone method [Windows Shell]","Clone method [Windows Shell]","ITravelLog interface","ITravelLog interface [Windows Shell]","Clone method","ITravelLog.Clone","ITravelLog::Clone","shdeprecated/ITravelLog::Clone","shell.ITravelLog_Clone","zone_ITravelLog_Clone"]
old-location: shell\ITravelLog_Clone.htm
tech.root: shell
ms.assetid: 546581f1-648d-4817-b3d2-aca219b74911
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],ITravelLog interface, ITravelLog interface [Windows Shell],Clone method, ITravelLog.Clone, ITravelLog::Clone, shdeprecated/ITravelLog::Clone, shell.ITravelLog_Clone, zone_ITravelLog_Clone
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - ITravelLog::Clone
 - shdeprecated/ITravelLog::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog.Clone
---

# ITravelLog::Clone


## -description

Deprecated. Duplicates the contents of the current travel log.

## -parameters

### -param pptl [out]

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>**</b>

The address of a pointer to the interface representing the cloned travel log.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.