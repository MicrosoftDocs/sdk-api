---
UID: NC:restartmanager.RM_WRITE_STATUS_CALLBACK
title: RM_WRITE_STATUS_CALLBACK
author: windows-driver-content
description: The RM_WRITE_STATUS_CALLBACK function can be implemented by the user interface that controls the Restart Manager.
old-location: rstmgr\rm_write_status_callback.htm
old-project: RstMgr
ms.assetid: 607a6b96-8509-4599-907c-edb8410d7921
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: RM_WRITE_STATUS_CALLBACK, RM_WRITE_STATUS_CALLBACK function pointer [Restart Mgr], restartmanager/RM_WRITE_STATUS_CALLBACK, rstmgr.rm_write_status_callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: restartmanager.h
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
req.typenames: IndexedResourceQualifier
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	RestartManager.h
api_name:
-	RM_WRITE_STATUS_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# RM_WRITE_STATUS_CALLBACK callback


## -description


The <b>RM_WRITE_STATUS_CALLBACK</b> function can be implemented by the user interface that controls the Restart Manager. The installer that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness. The percentage of completeness is strictly increasing and describes the current operation being performed and the name of the application being affected.


## -parameters




### -param nPercentComplete [in]

An integer value between 0 and 100 that indicates the percentage of the total number of applications that have either been shut down or restarted.


## -returns



This function pointer does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e0939b31-0233-40d2-96cf-bbabe9488a12">RmRestart</a>



<a href="https://msdn.microsoft.com/cdbc3bb7-0b3c-4fbc-8023-45a309c65bae">RmShutdown</a>
 

 

