---
UID: NF:comppkgsup.GetServerForPMP
title: GetServerForPMP function (comppkgsup.h)
description: Gets a COM server that has been registered for Protected Media Process (PMP) usage with previous call to RegisterServerForPMP.
helpviewer_keywords: ["GetServerForPMP","GetServerForPMP function [Windows API]","comppkgsup/GetServerForPMP","winprog.getserverforpmp"]
old-location: winprog\getserverforpmp.htm
tech.root: winprog
ms.assetid: 0E343396-A294-45E3-88E5-9B63EB8B10B9
ms.date: 12/05/2018
ms.keywords: GetServerForPMP, GetServerForPMP function [Windows API], comppkgsup/GetServerForPMP, winprog.getserverforpmp
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
 - GetServerForPMP
 - comppkgsup/GetServerForPMP
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
 - GetServerForPMP
---

# GetServerForPMP function


## -description

Gets a  COM server that has been registered  for Protected Media Process (PMP) usage with previous call to <a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-registerserverforpmp">RegisterServerForPMP</a>.

## -parameters

### -param serverClassId

The CLSID of the server to be retrieved.

### -param unknown [out]

Receives a pointer to the requested COM server interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.