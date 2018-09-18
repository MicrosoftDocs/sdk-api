---
UID: NE:mobsync._tagSYNCMGRINVOKEFLAGS
title: "_tagSYNCMGRINVOKEFLAGS"
author: windows-sdk-content
description: The SYNCMGRINVOKEFLAGS enumeration value specifies how the Sync Manager is to be invoked in the ISyncMgrSynchronizeInvoke::UpdateItems method.
old-location: shell\syncmgr_syncmgrinvokeflags.htm
tech.root: shell
ms.assetid: 6526e048-b7a8-4822-afd7-30f04a3039eb
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SYNCMGRINVOKEFLAGS, SYNCMGRINVOKEFLAGS enumeration [Windows Shell], SYNCMGRINVOKE_MINIMIZED, SYNCMGRINVOKE_STARTSYNC, _tagSYNCMGRINVOKEFLAGS, mobsync/SYNCMGRINVOKEFLAGS, mobsync/SYNCMGRINVOKE_MINIMIZED, mobsync/SYNCMGRINVOKE_STARTSYNC, shell.syncmgr_syncmgrinvokeflags, syncmgr.syncmgrinvokeflags
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
 - SYNCMGRINVOKEFLAGS
product: Windows
targetos: Windows
req.typenames: SYNCMGRINVOKEFLAGS
req.redist: 
---

# _tagSYNCMGRINVOKEFLAGS enumeration


## -description


The 
<b>SYNCMGRINVOKEFLAGS</b> enumeration value specifies how the Sync Manager is to be invoked in the 
<a href="https://msdn.microsoft.com/7a646d11-a84c-44c1-b52b-ffd364cc2ac3">ISyncMgrSynchronizeInvoke::UpdateItems</a> method.


## -enum-fields




### -field SYNCMGRINVOKE_STARTSYNC

Immediately start the synchronization without displaying the <b>Choice</b> dialog box.


### -field SYNCMGRINVOKE_MINIMIZED

Indicates that the <b>Choice</b> dialog should be minimized by default.


## -see-also




<a href="https://msdn.microsoft.com/7a646d11-a84c-44c1-b52b-ffd364cc2ac3">ISyncMgrSynchronizeInvoke::UpdateItems</a>
 

 

