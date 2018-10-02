---
UID: NF:wdsclientapi.WdsCliCreateSession
title: WdsCliCreateSession function
author: windows-sdk-content
description: Starts a new session with a WDS server.
old-location: wds\wdsclicreatesession.htm
tech.root: Wds
ms.assetid: c66801b2-ad5c-464b-ace3-269214621c20
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WdsCliCreateSession, WdsCliCreateSession function [Windows Deployment Services], wds.wdsclicreatesession, wdsclientapi/WdsCliCreateSession
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WdsCliCreateSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliCreateSession function


## -description


Starts a new session with a WDS server.


## -parameters




### -param pwszServer [in]

A pointer to a string value that contains the name or IP address of the WDS server.


### -param pCred [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/2aba59bf-3cd4-4376-b8c3-bb053ccd5c87">WDS_CLI_CRED</a> structure that contains the 
      client's credentials. This parameter can be null  for a session without authentication.


### -param phSession [out]

A pointer to a handle for the new session. This parameter is unmodified if the function is unsuccessful.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To close 
      the session and release resources, use the <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/2aba59bf-3cd4-4376-b8c3-bb053ccd5c87">WDS_CLI_CRED</a>



<a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

