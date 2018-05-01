---
UID: NC:smbclnt.SET_APP_INSTANCE_CSV_FLAGS
title: SET_APP_INSTANCE_CSV_FLAGS
author: windows-driver-content
description: Sets the flags that affect connections from the application instance.
old-location: mscs\setappinstancecsvflags.htm
old-project: MsCS
ms.assetid: 37FDAB0A-1593-47D6-B4CE-A667EBA01680
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SET_APP_INSTANCE_CSV_FLAGS, SET_APP_INSTANCE_CSV_FLAGS callback function [Failover Cluster], mscs.setappinstancecsvflags, smbclnt/SET_APP_INSTANCE_CSV_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: smbclnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SL_NONGENUINE_UI_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	SmbClnt.h
api_name:
-	SET_APP_INSTANCE_CSV_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# SET_APP_INSTANCE_CSV_FLAGS callback


## -description


Sets the flags that affect connections from the application instance.


## -parameters




### -param ProcessHandle [in]

A process handle for the current process or a remote process to be tagged with the 
      application instance. To tag a remote process, the handle must have 
      <b>PROCESS_TERMINATE</b> access to that process.


### -param Mask [in]

A bitmask that indicates the flags that are modified by the <i>Flags</i> parameter.


### -param Flags [in]

New values of the flags.


## -returns



Returns "0" if the operation is successful; otherwise, one of the following error codes is returned:




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

