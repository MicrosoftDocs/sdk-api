---
UID: NF:fhsvcctl.FhServiceOpenPipe
title: FhServiceOpenPipe function (fhsvcctl.h)
description: Opens a communication channel to the File History Service.
helpviewer_keywords: ["FhServiceOpenPipe","FhServiceOpenPipe function [Windows API]","fhsvcctl/FhServiceOpenPipe","winprog.fhserviceopenpipe"]
old-location: winprog\fhserviceopenpipe.htm
tech.root: winprog
ms.assetid: D0927124-0568-4897-9169-445C252E8ED4
ms.date: 12/05/2018
ms.keywords: FhServiceOpenPipe, FhServiceOpenPipe function [Windows API], fhsvcctl/FhServiceOpenPipe, winprog.fhserviceopenpipe
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
 - FhServiceOpenPipe
 - fhsvcctl/FhServiceOpenPipe
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
 - FhServiceOpenPipe
---

# FhServiceOpenPipe function


## -description

Opens a communication channel to the File History Service.

> [!NOTE] 
> **FhServiceOpenPipe** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param StartServiceIfStopped [in]

If the File History Service is not started yet and this parameter is <b>TRUE</b>, this function starts the File History Service before opening a communication channel to it.

If the File History Service is not started yet and this parameter is <b>FALSE</b>, this function fails and returns an unsuccessful <b>HRESULT</b> value.

### -param Pipe [out]

On successful return, this parameter contains a non-NULL handle representing a newly opened communication channel to the File History Service.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceclosepipe">FhServiceClosePipe</a>