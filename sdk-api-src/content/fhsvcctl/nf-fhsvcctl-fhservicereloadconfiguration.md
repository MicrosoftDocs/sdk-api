---
UID: NF:fhsvcctl.FhServiceReloadConfiguration
title: FhServiceReloadConfiguration function (fhsvcctl.h)
description: This function causes the File History Service to reload the current user’s File History configuration files.
helpviewer_keywords: ["FhServiceReloadConfiguration","FhServiceReloadConfiguration function [Windows API]","fhsvcctl/FhServiceReloadConfiguration","winprog.fhservicereloadconfiguration"]
old-location: winprog\fhservicereloadconfiguration.htm
tech.root: winprog
ms.assetid: DEFD729F-ED84-4C6A-8014-E986C2EB2767
ms.date: 12/05/2018
ms.keywords: FhServiceReloadConfiguration, FhServiceReloadConfiguration function [Windows API], fhsvcctl/FhServiceReloadConfiguration, winprog.fhservicereloadconfiguration
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
 - FhServiceReloadConfiguration
 - fhsvcctl/FhServiceReloadConfiguration
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
 - FhServiceReloadConfiguration
---

# FhServiceReloadConfiguration function


## -description

This function causes the File History Service to reload the current user’s File History configuration files.

> [!NOTE] 
> **FhServiceReloadConfiguration** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param Pipe [in]

The communication channel handle returned by an earlier <a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a> call.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

This function causes the File History Service to schedule periodic backups for the current user if they have not been scheduled yet and File History is enabled for that user.

It is recommended to call this function every time a policy is changed in File History configuration via the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a> method. It should also be called after File History has been enabled or disabled for a user.

## -see-also

<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhserviceopenpipe">FhServiceOpenPipe</a>



<a href="/windows/desktop/api/fhsvcctl/nf-fhsvcctl-fhservicestopbackup">FhServiceStopBackup</a>