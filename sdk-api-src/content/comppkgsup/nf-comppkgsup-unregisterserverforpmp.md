---
UID: NF:comppkgsup.UnregisterServerForPMP
title: UnregisterServerForPMP function (comppkgsup.h)
description: Registers a COM Server CLSID and a class factory that were previously registered for Protected Media Process (PMP) usage.
helpviewer_keywords: ["UnregisterServerForPMP","UnregisterServerForPMP function [Windows API]","comppkgsup/UnregisterServerForPMP","winprog.unregisterserverforpmp"]
old-location: winprog\unregisterserverforpmp.htm
tech.root: winprog
ms.assetid: FF89301E-FE17-4B14-872E-271BDB85A784
ms.date: 12/05/2018
ms.keywords: UnregisterServerForPMP, UnregisterServerForPMP function [Windows API], comppkgsup/UnregisterServerForPMP, winprog.unregisterserverforpmp
req.header: comppkgsup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comppkgsup.lib
req.dll: CompPkgSup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterServerForPMP
 - comppkgsup/UnregisterServerForPMP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CompPkgSup.dll
api_name:
 - UnregisterServerForPMP
---

# UnregisterServerForPMP function


## -description

Registers a COM Server CLSID and a class factory that were previously registered for Protected Media Process (PMP) usage.

## -parameters

### -param token

The registration token obtained from a previous call to <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-registerserverforpmp">RegisterServerForPMP</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.