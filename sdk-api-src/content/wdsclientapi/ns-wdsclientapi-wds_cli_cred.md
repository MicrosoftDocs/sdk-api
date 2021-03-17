---
UID: NS:wdsclientapi.tagWDS_CLI_CRED
title: WDS_CLI_CRED (wdsclientapi.h)
description: Contains credentials used to authorize a client session.
helpviewer_keywords: ["*LPWDS_CLI_CRED","*PWDS_CLI_CRED","LPWDS_CLI_CRED","LPWDS_CLI_CRED structure pointer [Windows Deployment Services]","PWDS_CLI_CRED","PWDS_CLI_CRED structure pointer [Windows Deployment Services]","WDS_CLI_CRED","WDS_CLI_CRED structure [Windows Deployment Services]","wds.wds_cli_cred","wdsclientapi/LPWDS_CLI_CRED","wdsclientapi/PWDS_CLI_CRED","wdsclientapi/WDS_CLI_CRED"]
old-location: wds\wds_cli_cred.htm
tech.root: wds
ms.assetid: 2aba59bf-3cd4-4376-b8c3-bb053ccd5c87
ms.date: 12/05/2018
ms.keywords: '*LPWDS_CLI_CRED, *PWDS_CLI_CRED, LPWDS_CLI_CRED, LPWDS_CLI_CRED structure pointer [Windows Deployment Services], PWDS_CLI_CRED, PWDS_CLI_CRED structure pointer [Windows Deployment Services], WDS_CLI_CRED, WDS_CLI_CRED structure [Windows Deployment Services], wds.wds_cli_cred, wdsclientapi/LPWDS_CLI_CRED, wdsclientapi/PWDS_CLI_CRED, wdsclientapi/WDS_CLI_CRED'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWDS_CLI_CRED
 - wdsclientapi/tagWDS_CLI_CRED
 - PWDS_CLI_CRED
 - wdsclientapi/PWDS_CLI_CRED
 - WDS_CLI_CRED
 - wdsclientapi/WDS_CLI_CRED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsClientAPI.h
api_name:
 - WDS_CLI_CRED
---

# WDS_CLI_CRED structure


## -description

Contains credentials used to authorize a client session.

## -struct-fields

### -field pwszUserName

The user name associated with the credentials.

### -field pwszDomain

The domain for the user name associated with the credentials.

### -field pwszPassword

The password for the user name associated with the credentials.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliauthorizesession">WdsCliAuthorizeSession</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a>



<a href="/windows/desktop/Wds/windows-deployment-services-structures">Windows Deployment Services Structures</a>