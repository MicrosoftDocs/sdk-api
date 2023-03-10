---
UID: NF:fhsvcctl.FhServiceBlockBackup
title: FhServiceBlockBackup function (fhsvcctl.h)
description: This function temporarily blocks backups for the current user.
helpviewer_keywords: ["FhServiceBlockBackup","FhServiceBlockBackup function [Windows API]","fhsvcctl/FhServiceBlockBackup","winprog.fhserviceblockbackup"]
old-location: winprog\fhserviceblockbackup.htm
tech.root: winprog
ms.assetid: 32B5E241-5A5F-4440-9B47-07D5849FA393
ms.date: 12/05/2018
ms.keywords: FhServiceBlockBackup, FhServiceBlockBackup function [Windows API], fhsvcctl/FhServiceBlockBackup, winprog.fhserviceblockbackup
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
 - FhServiceBlockBackup
 - fhsvcctl/FhServiceBlockBackup
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
 - FhServiceBlockBackup
---

# FhServiceBlockBackup function


## -description

This function temporarily blocks backups for the current user.

> [!NOTE] 
> **FhServiceBlockBackup** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

This function instructs the File History Service to not perform backups for the current user until the <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceunblockbackup">FhServiceUnblockBackup</a> function is called or the communication channel with the File History Service is closed by calling <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceclosepipe">FhServiceClosePipe</a>.

Call this function prior to performing File History configuration reassociation to ensure that File History configuration and data files are not currently in use. (Otherwise, the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a> method may fail.)

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceclosepipe">FhServiceClosePipe</a>



<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>



<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceunblockbackup">FhServiceUnblockBackup</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhreassociation-performreassociation">IFhReassociation::PerformReassociation</a>