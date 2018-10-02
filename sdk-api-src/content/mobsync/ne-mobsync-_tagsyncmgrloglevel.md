---
UID: NE:mobsync._tagSYNCMGRLOGLEVEL
title: "_tagSYNCMGRLOGLEVEL"
author: windows-sdk-content
description: The SYNCMGRLOGLEVEL enumeration values specify an error level for use in the ISyncMgrSynchronizeCallback::LogError method.
old-location: shell\syncmgr_syncmgrloglevel.htm
tech.root: Shell
ms.assetid: df3c3300-e203-4664-b8d5-9dc4835b33d8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: SYNCMGRLOGLEVEL, SYNCMGRLOGLEVEL enumeration [Windows Shell], SYNCMGRLOGLEVEL_ERROR, SYNCMGRLOGLEVEL_INFORMATION, SYNCMGRLOGLEVEL_LOGLEVELMAX, SYNCMGRLOGLEVEL_WARNING, _tagSYNCMGRLOGLEVEL, mobsync/SYNCMGRLOGLEVEL, mobsync/SYNCMGRLOGLEVEL_ERROR, mobsync/SYNCMGRLOGLEVEL_INFORMATION, mobsync/SYNCMGRLOGLEVEL_LOGLEVELMAX, mobsync/SYNCMGRLOGLEVEL_WARNING, shell.syncmgr_syncmgrloglevel, syncmgr.syncmgrloglevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Mobsync.h
api_name:
 - SYNCMGRLOGLEVEL
product: Windows
targetos: Windows
req.typenames: SYNCMGRLOGLEVEL
req.redist: 
---

# _tagSYNCMGRLOGLEVEL enumeration


## -description


The 
<b>SYNCMGRLOGLEVEL</b> enumeration values specify an error level for use in the 
<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a> method.


## -enum-fields




### -field SYNCMGRLOGLEVEL_INFORMATION

An information message was logged.


### -field SYNCMGRLOGLEVEL_WARNING

A warning message was logged.


### -field SYNCMGRLOGLEVEL_ERROR

An error message was logged.


### -field SYNCMGRLOGLEVEL_LOGLEVELMAX

The largest valid <a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a> value.


## -see-also




<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a>
 

 

