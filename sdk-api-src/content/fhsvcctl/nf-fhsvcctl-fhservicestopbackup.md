---
UID: NF:fhsvcctl.FhServiceStopBackup
title: FhServiceStopBackup function (fhsvcctl.h)
description: This function stops an ongoing backup cycle for the current user.
helpviewer_keywords: ["FhServiceStopBackup","FhServiceStopBackup function [Windows API]","fhsvcctl/FhServiceStopBackup","winprog.fhservicestopbackup"]
old-location: winprog\fhservicestopbackup.htm
tech.root: winprog
ms.assetid: 17FCD464-2543-454A-B60E-E37EDF61C595
ms.date: 12/05/2018
ms.keywords: FhServiceStopBackup, FhServiceStopBackup function [Windows API], fhsvcctl/FhServiceStopBackup, winprog.fhservicestopbackup
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
 - FhServiceStopBackup
 - fhsvcctl/FhServiceStopBackup
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
 - FhServiceStopBackup
---

# FhServiceStopBackup function


## -description

This function stops an ongoing backup cycle for the current user.

> [!NOTE] 
> **FhServiceStopBackup** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

### -param StopTracking [in]

If <b>TRUE</b>, this function both stops the ongoing backup cycle (if any) and prevents periodic backup cycles for the current user in the future.

If <b>FALSE</b>, this function only stops the ongoing backup cycle.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>