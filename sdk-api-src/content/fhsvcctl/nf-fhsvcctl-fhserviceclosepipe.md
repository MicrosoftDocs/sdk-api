---
UID: NF:fhsvcctl.FhServiceClosePipe
title: FhServiceClosePipe function (fhsvcctl.h)
description: Closes a communication channel to the File History Service opened with FhServiceOpenPipe.
helpviewer_keywords: ["FhServiceClosePipe","FhServiceClosePipe function [Windows API]","fhsvcctl/FhServiceClosePipe","winprog.fhserviceclosepipe"]
old-location: winprog\fhserviceclosepipe.htm
tech.root: winprog
ms.assetid: 20C46E2A-E79F-47B9-9D7A-74CD3AF03EF7
ms.date: 12/05/2018
ms.keywords: FhServiceClosePipe, FhServiceClosePipe function [Windows API], fhsvcctl/FhServiceClosePipe, winprog.fhserviceclosepipe
req.header: fhsvcctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FhSvcCtl.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FhServiceClosePipe
 - fhsvcctl/FhServiceClosePipe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - FhSvcCtl.lib
 - FhSvcCtl.dll
api_name:
 - FhServiceClosePipe
---

# FhServiceClosePipe function


## -description

Closes a communication channel to the File History Service opened with <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>.

> [!NOTE] 
> **FhServiceClosePipe** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

An application should call <b>FhServiceClosePipe</b> once for each communication channel handle it opens with <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>. Closing a communication channel handle multiple times is not supported and may lead to unpredictable behavior.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>