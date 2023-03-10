---
UID: NC:restartmanager.RM_WRITE_STATUS_CALLBACK
title: RM_WRITE_STATUS_CALLBACK (restartmanager.h)
description: The RM_WRITE_STATUS_CALLBACK function can be implemented by the user interface that controls the Restart Manager.
helpviewer_keywords: ["RM_WRITE_STATUS_CALLBACK","RM_WRITE_STATUS_CALLBACK callback","RM_WRITE_STATUS_CALLBACK callback function [Restart Mgr]","restartmanager/RM_WRITE_STATUS_CALLBACK","rstmgr.rm_write_status_callback"]
old-location: rstmgr\rm_write_status_callback.htm
tech.root: rstmgr
ms.assetid: 607a6b96-8509-4599-907c-edb8410d7921
ms.date: 12/05/2018
ms.keywords: RM_WRITE_STATUS_CALLBACK, RM_WRITE_STATUS_CALLBACK callback, RM_WRITE_STATUS_CALLBACK callback function [Restart Mgr], restartmanager/RM_WRITE_STATUS_CALLBACK, rstmgr.rm_write_status_callback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RM_WRITE_STATUS_CALLBACK
 - restartmanager/RM_WRITE_STATUS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - RestartManager.h
api_name:
 - RM_WRITE_STATUS_CALLBACK
---

# RM_WRITE_STATUS_CALLBACK callback function


## -description

The <b>RM_WRITE_STATUS_CALLBACK</b> function can be implemented by the user interface that controls the Restart Manager. The installer that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness. The percentage of completeness is strictly increasing and describes the current operation being performed and the name of the application being affected.

## -parameters

### -param nPercentComplete [in]

An integer value between 0 and 100 that indicates the percentage of the total number of applications that have either been shut down or restarted.

## -see-also

<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmrestart">RmRestart</a>



<a href="/windows/desktop/api/restartmanager/nf-restartmanager-rmshutdown">RmShutdown</a>