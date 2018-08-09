---
UID: NE:syncmgr.SYNCMGR_RESOLUTION_FEEDBACK
title: SYNCMGR_RESOLUTION_FEEDBACK
author: windows-sdk-content
description: Describes Sync Manager resolution feedback. Used by ISyncMgrResolutionHandler.
old-location: shell\SYNCMGR_RESOLUTION_FEEDBACK.htm
old-project: shell
ms.assetid: 9526cac8-0df3-40b2-9f86-1a4dadb61dcc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SYNCMGR_RESOLUTION_FEEDBACK, SYNCMGR_RESOLUTION_FEEDBACK enumeration [Windows Shell], SYNCMGR_RF_CANCEL, SYNCMGR_RF_CONTINUE, SYNCMGR_RF_REFRESH, _shell_SYNCMGR_RESOLUTION_FEEDBACK, shell.SYNCMGR_RESOLUTION_FEEDBACK, syncmgr/SYNCMGR_RESOLUTION_FEEDBACK, syncmgr/SYNCMGR_RF_CANCEL, syncmgr/SYNCMGR_RF_CONTINUE, syncmgr/SYNCMGR_RF_REFRESH
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNCMGR_RESOLUTION_FEEDBACK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_RESOLUTION_FEEDBACK
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# SYNCMGR_RESOLUTION_FEEDBACK enumeration


## -description


Describes Sync Manager resolution feedback. Used by <a href="https://msdn.microsoft.com/5b77217d-5c63-41be-b4df-338714a90fb9">ISyncMgrResolutionHandler</a>.


## -enum-fields




### -field SYNCMGR_RF_CONTINUE

Proceed to the next conflict.


### -field SYNCMGR_RF_REFRESH

<b>Apply to All</b> is stopped and the dialog will be displayed for this conflict.


### -field SYNCMGR_RF_CANCEL

 Cancels resolution of any more conflicts in the set.

