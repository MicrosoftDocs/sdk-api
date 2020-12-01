---
UID: NF:wdsclientapi.WdsCliAuthorizeSession
title: WdsCliAuthorizeSession function (wdsclientapi.h)
description: Converts a session with a WDS server into an authenticated session.
helpviewer_keywords: ["WdsCliAuthorizeSession","WdsCliAuthorizeSession function [Windows Deployment Services]","wds.wdscliauthorizesession","wdsclientapi/WdsCliAuthorizeSession"]
old-location: wds\wdscliauthorizesession.htm
tech.root: wds
ms.assetid: 88e95fa8-1a83-4ef9-b486-c8086cb08116
ms.date: 12/05/2018
ms.keywords: WdsCliAuthorizeSession, WdsCliAuthorizeSession function [Windows Deployment Services], wds.wdscliauthorizesession, wdsclientapi/WdsCliAuthorizeSession
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliAuthorizeSession
 - wdsclientapi/WdsCliAuthorizeSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliAuthorizeSession
---

# WdsCliAuthorizeSession function


## -description

Converts a session with a WDS server into an authenticated session.

## -parameters

### -param hSession [in, out]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a> function.

### -param pCred [in, optional]

Pointer to a <a href="/windows/desktop/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred">WDS_CLI_CRED</a> structure that contains the 
      client's credentials.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred">WDS_CLI_CRED</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>