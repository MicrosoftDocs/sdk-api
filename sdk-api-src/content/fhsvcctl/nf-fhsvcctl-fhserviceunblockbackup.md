---
UID: NF:fhsvcctl.FhServiceUnblockBackup
title: FhServiceUnblockBackup function (fhsvcctl.h)
description: This function unblocks backups blocked via FhServiceBlockBackup.
helpviewer_keywords: ["FhServiceUnblockBackup","FhServiceUnblockBackup function [Windows API]","fhsvcctl/FhServiceUnblockBackup","winprog.fhserviceunblockbackup"]
old-location: winprog\fhserviceunblockbackup.htm
tech.root: winprog
ms.assetid: 4CCCEEA5-40BC-4862-ADF5-C8757E02916A
ms.date: 12/05/2018
ms.keywords: FhServiceUnblockBackup, FhServiceUnblockBackup function [Windows API], fhsvcctl/FhServiceUnblockBackup, winprog.fhserviceunblockbackup
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
 - FhServiceUnblockBackup
 - fhsvcctl/FhServiceUnblockBackup
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
 - FhServiceUnblockBackup
---

# FhServiceUnblockBackup function


## -description

This function unblocks backups blocked via <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceblockbackup">FhServiceBlockBackup</a>.

> [!NOTE] 
> **FhServiceUnblockBackup** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

This function removes the effects of a prior <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceblockbackup">FhServiceBlockBackup</a> call issued via a given communication channel with the File History Service.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceblockbackup">FhServiceBlockBackup</a>



<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>