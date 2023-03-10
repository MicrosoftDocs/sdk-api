---
UID: NF:comppkgsup.RegisterServerForPMP
title: RegisterServerForPMP function (comppkgsup.h)
description: Registers a COM Server CLSID and a class factory for Protected Media Process (PMP) usage.
helpviewer_keywords: ["RegisterServerForPMP","RegisterServerForPMP function [Windows API]","comppkgsup/RegisterServerForPMP","winprog.registerserverforpmp"]
old-location: winprog\registerserverforpmp.htm
tech.root: winprog
ms.assetid: F18A5596-F21E-427B-8281-544DD7CA9E0B
ms.date: 12/05/2018
ms.keywords: RegisterServerForPMP, RegisterServerForPMP function [Windows API], comppkgsup/RegisterServerForPMP, winprog.registerserverforpmp
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
 - RegisterServerForPMP
 - comppkgsup/RegisterServerForPMP
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
 - RegisterServerForPMP
---

# RegisterServerForPMP function


## -description

Registers a COM Server CLSID and a class factory for Protected Media Process (PMP) usage.

## -parameters

### -param serverClassId

The CLSID of the COM server to be registered.

### -param classFactory

The class factory to be registered.

### -param token [out]

Receives a pointer to a registration token that can be used to unregister the server with <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-unregisterserverforpmp">UnregisterServerForPMP</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.