---
UID: NF:wdsclientapi.WdsCliAuthorizeSession
title: WdsCliAuthorizeSession function
author: windows-sdk-content
description: Converts a session with a WDS server into an authenticated session.
old-location: wds\wdscliauthorizesession.htm
tech.root: wds
ms.assetid: 88e95fa8-1a83-4ef9-b486-c8086cb08116
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WdsCliAuthorizeSession, WdsCliAuthorizeSession function [Windows Deployment Services], wds.wdscliauthorizesession, wdsclientapi/WdsCliAuthorizeSession
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliAuthorizeSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliAuthorizeSession function


## -description


Converts a session with a WDS server into an authenticated session.


## -parameters




### -param hSession [in, out]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a> function.


### -param pCred [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/2aba59bf-3cd4-4376-b8c3-bb053ccd5c87">WDS_CLI_CRED</a> structure that contains the 
      client's credentials. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/2aba59bf-3cd4-4376-b8c3-bb053ccd5c87">WDS_CLI_CRED</a>



<a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

