---
UID: NF:wdsclientapi.WdsCliCreateSession
title: WdsCliCreateSession function (wdsclientapi.h)
description: Starts a new session with a WDS server.
helpviewer_keywords: ["WdsCliCreateSession","WdsCliCreateSession function [Windows Deployment Services]","wds.wdsclicreatesession","wdsclientapi/WdsCliCreateSession"]
old-location: wds\wdsclicreatesession.htm
tech.root: wds
ms.assetid: c66801b2-ad5c-464b-ace3-269214621c20
ms.date: 12/05/2018
ms.keywords: WdsCliCreateSession, WdsCliCreateSession function [Windows Deployment Services], wds.wdsclicreatesession, wdsclientapi/WdsCliCreateSession
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
 - WdsCliCreateSession
 - wdsclientapi/WdsCliCreateSession
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
 - WdsCliCreateSession
---

# WdsCliCreateSession function


## -description

Starts a new session with a WDS server.

## -parameters

### -param pwszServer [in]

A pointer to a string value that contains the name or IP address of the WDS server.

### -param pCred [in, optional]

A pointer to a <a href="/windows/desktop/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred">WDS_CLI_CRED</a> structure that contains the 
      client's credentials. This parameter can be null  for a session without authentication.

### -param phSession [out]

A pointer to a handle for the new session. This parameter is unmodified if the function is unsuccessful.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To close 
      the session and release resources, use the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred">WDS_CLI_CRED</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>