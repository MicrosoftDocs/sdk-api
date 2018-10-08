---
UID: NE:syncmgr.SYNCMGR_HANDLER_POLICIES
title: SYNCMGR_HANDLER_POLICIES
author: windows-sdk-content
description: Enumerates policies specified by a sync handler that deviate from the default policy.
old-location: shell\SYNCMGR_HANDLER_POLICIES.htm
tech.root: shell
ms.assetid: 2baf39ea-2b28-4d38-8635-8f5efca54702
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SYNCMGR_HANDLER_POLICIES, SYNCMGR_HANDLER_POLICIES enumeration [Windows Shell], SYNCMGR_HPM_BACKGROUND_SYNC_ONLY, SYNCMGR_HPM_DISABLE_BROWSE, SYNCMGR_HPM_DISABLE_DISABLE, SYNCMGR_HPM_DISABLE_ENABLE, SYNCMGR_HPM_DISABLE_SCHEDULE, SYNCMGR_HPM_DISABLE_START_SYNC, SYNCMGR_HPM_DISABLE_STOP_SYNC, SYNCMGR_HPM_HIDDEN_BY_DEFAULT, SYNCMGR_HPM_NONE, SYNCMGR_HPM_PREVENT_ACTIVATE, SYNCMGR_HPM_PREVENT_DEACTIVATE, SYNCMGR_HPM_PREVENT_DISABLE, SYNCMGR_HPM_PREVENT_ENABLE, SYNCMGR_HPM_PREVENT_START_SYNC, SYNCMGR_HPM_PREVENT_STOP_SYNC, SYNCMGR_HPM_VALID_MASK, shell.SYNCMGR_HANDLER_POLICIES, shell_SYNCMGR_HANDLER_POLICIES, syncmgr/SYNCMGR_HANDLER_POLICIES, syncmgr/SYNCMGR_HPM_BACKGROUND_SYNC_ONLY, syncmgr/SYNCMGR_HPM_DISABLE_BROWSE, syncmgr/SYNCMGR_HPM_DISABLE_DISABLE, syncmgr/SYNCMGR_HPM_DISABLE_ENABLE, syncmgr/SYNCMGR_HPM_DISABLE_SCHEDULE, syncmgr/SYNCMGR_HPM_DISABLE_START_SYNC, syncmgr/SYNCMGR_HPM_DISABLE_STOP_SYNC, syncmgr/SYNCMGR_HPM_HIDDEN_BY_DEFAULT, syncmgr/SYNCMGR_HPM_NONE, syncmgr/SYNCMGR_HPM_PREVENT_ACTIVATE, syncmgr/SYNCMGR_HPM_PREVENT_DEACTIVATE, syncmgr/SYNCMGR_HPM_PREVENT_DISABLE, syncmgr/SYNCMGR_HPM_PREVENT_ENABLE, syncmgr/SYNCMGR_HPM_PREVENT_START_SYNC, syncmgr/SYNCMGR_HPM_PREVENT_STOP_SYNC, syncmgr/SYNCMGR_HPM_VALID_MASK
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_HANDLER_POLICIES
product: Windows
targetos: Windows
req.typenames: SYNCMGR_HANDLER_POLICIES
req.redist: 
---

# SYNCMGR_HANDLER_POLICIES enumeration


## -description


Enumerates policies specified by a sync handler that deviate from the default policy.


## -enum-fields




### -field SYNCMGR_HPM_NONE

No handler policy flags are set.


### -field SYNCMGR_HPM_PREVENT_ACTIVATE

Activation of the handler is not supported at the time of the call. This value can be used by a handler to implement support for group policy that prevents the handler from being activated. If this value is set, the <b>Setup</b> task is not be shown in the Setup Sync folder when this handler is selected. The handler should provide a comment—returned from its implementation of <a href="https://msdn.microsoft.com/755d3038-934f-42b7-a807-7037fa0ea21e">ISyncMgrHandlerInfo::GetComment</a>—to let the user know why the <b>Setup</b> task is not available. Most handlers should not set this value.


### -field SYNCMGR_HPM_PREVENT_DEACTIVATE

Deactivation of the handler is not supported at the time of the call. This value can be used by a handler to implement support for group policy that prevents the handler from being deactivated. If this value is set, the <b>Delete</b> task is not shown in the Sync Center folder when this handler is selected. The handler should provide a comment—returned from its implementation of <a href="https://msdn.microsoft.com/755d3038-934f-42b7-a807-7037fa0ea21e">ISyncMgrHandlerInfo::GetComment</a>—to let the user know why the <b>Setup</b> task is not available. Most handlers should not set this value.


### -field SYNCMGR_HPM_PREVENT_ENABLE

The handler normally supports enable, but cannot be enabled because of handler policy. If this flag is set, the <b>Enable</b> option will not be displayed on the context menu.


### -field SYNCMGR_HPM_PREVENT_DISABLE

The handler normally supports disable, but cannot be enabled because of handler policy. If this flag is set, the <b>Disable</b> option will not be displayed on the context menu.


### -field SYNCMGR_HPM_PREVENT_START_SYNC

The handler normally supports sync, but cannot be synchronized because of handler policy. If this flag is set, the <b>Start Sync</b> option will not be displayed on the context menu or the command bar.


### -field SYNCMGR_HPM_PREVENT_STOP_SYNC

The handler normally supports sync, but cannot be synchronized because of handler policy. If this flag is set, the <b>Stop Sync</b> option will not be displayed on the context menu or the command bar.


### -field SYNCMGR_HPM_DISABLE_ENABLE

The handler normally supports enable, but cannot be enabled at the time of the call. The <b>Enable</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_DISABLE_DISABLE

The handler normally supports disable, but cannot be disabled at the time of the call. The <b>Disable</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_DISABLE_START_SYNC

The handler normally supports syncing, but cannot be synchronized at the time of the call. The <b>Start Sync</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_DISABLE_STOP_SYNC

The handler normally supports cancel, but cannot be canceled at the time of the call. The <b>Stop Sync</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_DISABLE_BROWSE

The handler normally supports cancel, but cannot be canceled at the time of the call. The <b>Browse</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_DISABLE_SCHEDULE

The handler normally supports cancel, but cannot be canceled at the time of the call. The <b>Show Schedule</b> option will be displayed but will be disabled.


### -field SYNCMGR_HPM_HIDDEN_BY_DEFAULT

The handler should be hidden from the user unless the <b>Show Hidden Files</b> option has been enabled. This policy only applies the first time that the handler is loaded. After that, the hidden state is maintained by Sync Center and can be changed by the user through the property sheet. The hidden state is available in the folder UI as the System.Sync.Hidden (PKEY_Sync_Hidden) property.


### -field SYNCMGR_HPM_BACKGROUND_SYNC_ONLY

The user is not offered <b>Sync</b> and <b>Stop</b> tasks in the UI. This is equivalent to <code>SYNCMGR_HPM_PREVENT_START_SYNC | SYNCMGR_HPM_PREVENT_STOP_SYNC</code>.


### -field SYNCMGR_HPM_VALID_MASK

A mask used to retrieve valid <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_HANDLER_POLICIES</a> flags.

