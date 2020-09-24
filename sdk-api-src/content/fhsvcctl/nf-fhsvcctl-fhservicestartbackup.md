---
UID: NF:fhsvcctl.FhServiceStartBackup
title: FhServiceStartBackup function (fhsvcctl.h)
description: This function starts an immediate backup for the current user.
helpviewer_keywords: ["FhServiceStartBackup","FhServiceStartBackup function [Windows API]","fhsvcctl/FhServiceStartBackup","winprog.fhservicestartbackup"]
old-location: winprog\fhservicestartbackup.htm
tech.root: winprog
ms.assetid: 30800744-8605-4F8B-9B7A-50F57CC73483
ms.date: 12/05/2018
ms.keywords: FhServiceStartBackup, FhServiceStartBackup function [Windows API], fhsvcctl/FhServiceStartBackup, winprog.fhservicestartbackup
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
 - FhServiceStartBackup
 - fhsvcctl/FhServiceStartBackup
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
 - FhServiceStartBackup
---

# FhServiceStartBackup function


## -description

This function starts an immediate backup for the current user.

> [!NOTE] 
> **FhServiceStartBackup** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

### -param LowPriorityIo [in]

If <b>TRUE</b>, the File History Service is instructed to use low priority I/O for the immediate backup scheduled by this function. Low-priority I/O reduces impact on foreground user activities. It is recommended to set this parameter to <b>TRUE.</b>

If <b>FALSE</b>, the File History Service is instructed to use normal priority I/O for the immediate backup scheduled by this function. This results in faster backups but negatively affects the responsiveness and performance of user applications.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

This function does not wait until the immediate backup completes. If an error or warning condition is encountered during backup, it is communicated to the user via an Action Center notification and programmatically retrievable via the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-queryprotectionstatus">IFhConfigMgr::QueryProtectionStatus</a> method.

A backup cycle initiated by calling this function can be stopped using the <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhservicestopbackup">FhServiceStopBackup</a> function.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>



<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhservicestopbackup">FhServiceStopBackup</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-queryprotectionstatus">IFhConfigMgr::QueryProtectionStatus</a>