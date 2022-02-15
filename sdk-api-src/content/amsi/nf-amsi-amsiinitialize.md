---
UID: NF:amsi.AmsiInitialize
title: AmsiInitialize function (amsi.h)
description: Initialize the AMSI API.
helpviewer_keywords: ["AmsiInitialize","AmsiInitialize function [Antimalware Scan Interface]","amsi.amsiinitialize","amsi/AmsiInitialize"]
old-location: amsi\amsiinitialize.htm
tech.root: AMSI
ms.assetid: 946FC79C-556C-404E-A559-323AA69B3EC6
ms.date: 12/05/2018
ms.keywords: AmsiInitialize, AmsiInitialize function [Antimalware Scan Interface], amsi.amsiinitialize, amsi/AmsiInitialize
req.header: amsi.h
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
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AmsiInitialize
 - amsi/AmsiInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiInitialize
---

## -description

Initialize the AMSI API.

## -parameters

### -param appName [in]

The name, version, or GUID string of the app calling the AMSI API.

### -param amsiContext [out]

A handle of type HAMSICONTEXT that must be passed to all subsequent calls to the AMSI API.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the app is finished with the AMSI API it must call <a href="/windows/desktop/api/amsi/nf-amsi-amsiuninitialize">AmsiUninitialize</a>.

## -see-also

<a href="/windows/desktop/api/amsi/nf-amsi-amsiuninitialize">AmsiUninitialize</a>