---
UID: NS:wdsclientapi.tagWDS_CLI_CRED
title: tagWDS_CLI_CRED
author: windows-sdk-content
description: Contains credentials used to authorize a client session.
old-location: wds\wds_cli_cred.htm
tech.root: Wds
ms.assetid: 2aba59bf-3cd4-4376-b8c3-bb053ccd5c87
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPWDS_CLI_CRED, *PWDS_CLI_CRED, LPWDS_CLI_CRED, LPWDS_CLI_CRED structure pointer [Windows Deployment Services], PWDS_CLI_CRED, PWDS_CLI_CRED structure pointer [Windows Deployment Services], WDS_CLI_CRED, WDS_CLI_CRED structure [Windows Deployment Services], tagWDS_CLI_CRED, wds.wds_cli_cred, wdsclientapi/LPWDS_CLI_CRED, wdsclientapi/PWDS_CLI_CRED, wdsclientapi/WDS_CLI_CRED"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsClientAPI.h
api_name:
 - WDS_CLI_CRED
product: Windows
targetos: Windows
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
req.redist: 
---

# tagWDS_CLI_CRED structure


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




<a href="https://msdn.microsoft.com/88e95fa8-1a83-4ef9-b486-c8086cb08116">WdsCliAuthorizeSession</a>



<a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a>



<a href="https://msdn.microsoft.com/2e52a6ae-cecb-45de-b777-108836ed5264">Windows Deployment Services Structures</a>
 

 

