---
UID: NE:ntdsapi.DS_REPSYNCALL_ERROR
title: DS_REPSYNCALL_ERROR
author: windows-sdk-content
description: The DS_REPSYNCALL_ERROR enumeration is used with the DS_REPSYNCALL_ERRINFO structure to indicate where in the replication process an error occurred.
old-location: ad\ds_repsyncall_error.htm
tech.root: ad
ms.assetid: 9c020046-ab52-4676-931e-12ce176e93fb
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: DS_REPSYNCALL_ERROR, DS_REPSYNCALL_ERROR enumeration [Active Directory], DS_REPSYNCALL_SERVER_UNREACHABLE, DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER, DS_REPSYNCALL_WIN32_ERROR_REPLICATING, ad.ds_repsyncall_error, ntdsapi/DS_REPSYNCALL_ERROR, ntdsapi/DS_REPSYNCALL_SERVER_UNREACHABLE, ntdsapi/DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER, ntdsapi/DS_REPSYNCALL_WIN32_ERROR_REPLICATING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - Ntdsapi.h
api_name:
 - DS_REPSYNCALL_ERROR
product: Windows
targetos: Windows
req.typenames: DS_REPSYNCALL_ERROR
req.redist: 
---

# DS_REPSYNCALL_ERROR enumeration


## -description


The <b>DS_REPSYNCALL_ERROR</b> enumeration is used with the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure to indicate where in the replication process an error occurred.


## -enum-fields




### -field DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER

The server referred to by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.


### -field DS_REPSYNCALL_WIN32_ERROR_REPLICATING

An error occurred during replication of the server identified by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure.


### -field DS_REPSYNCALL_SERVER_UNREACHABLE

The server identified by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.


## -see-also




<a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a>



<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a>
 

 

