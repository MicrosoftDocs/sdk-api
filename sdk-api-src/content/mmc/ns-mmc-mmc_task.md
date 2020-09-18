---
UID: NS:mmc._MMC_TASK
title: MMC_TASK (mmc.h)
description: The MMC_TASK structure is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_ACTION_ID","MMC_ACTION_LINK","MMC_ACTION_SCRIPT","MMC_TASK","MMC_TASK structure [MMC]","_slate_mmc_task","mmc.mmc_task","mmc/MMC_TASK"]
old-location: mmc\mmc_task.htm
tech.root: mmc
ms.assetid: bb101c09-947f-4316-890a-86e09358d88c
ms.date: 12/05/2018
ms.keywords: MMC_ACTION_ID, MMC_ACTION_LINK, MMC_ACTION_SCRIPT, MMC_TASK, MMC_TASK structure [MMC], _slate_mmc_task, mmc.mmc_task, mmc/MMC_TASK
req.header: mmc.h
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
targetos: Windows
req.typenames: MMC_TASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_TASK
 - mmc/_MMC_TASK
 - MMC_TASK
 - mmc/MMC_TASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_TASK
---

# MMC_TASK structure


## -description

The 
<b>MMC_TASK</b> structure is introduced in MMC 1.1.

The 
<b>MMC_TASK</b> structure is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a> method to specify all the data required to set up an individual task on a taskpad.

## -struct-fields

### -field sDisplayObject

<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure that the snap-in must fill in to specify the image to be displayed as the image for the task in the taskpad specified by <b>pszGroup</b>.

### -field szText

A pointer to a null-terminated string that contains the text placed directly to the right of the mouse-over image. This text serves as the label for the task. This text should be an action in the imperative such as "Add a new user."

### -field szHelpString

A pointer to a null-terminated string that contains the descriptive text placed in the upper-right corner when the user moves the mouse over the mouse-over image or the label text for the task. This text serves as the description for the task such as "Creates a new account, creates a mailbox, and sets up everything a user must access the network."

### -field eActionType

Value of type 
<a href="/windows/desktop/api/mmc/ne-mmc-mmc_action_type">MMC_ACTION_TYPE</a> that specifies the type of action triggered when a user clicks a task on a taskpad.

There are three types of actions:



#### MMC_ACTION_ID

When the user clicks the task, MMC calls 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> and returns the command ID specified in the <b>nCommandID</b> member. If you specify this value, the <b>nCommandID</b> member is required.



#### MMC_ACTION_LINK

When the user clicks the task, MMC activates the link specified by <b>szActionURL</b>. If you specify this value, the <b>szActionURL</b> member is required.



#### MMC_ACTION_SCRIPT

When the user clicks the task, MMC executes the script contained in <b>szScript</b> using the <a href="/previous-versions/hh869591(v=vs.85)">window.execScript</a> method on the taskpad DHTML page. If you specify this value, the <b>zScript</b> member is required.

### -field nCommandID

Used only if <b>eActionType</b> is <b>MMC_ACTION_ID</b>.

A value that specifies the command ID returned to the snap-in when the user clicks the task.

When MMC calls <a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a>, it passes in the <i>arg</i> parameter a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure that contains the command ID for the task that was clicked on the taskpad. The <b>vt</b> field is <b>VT_I4</b> and the <b>lVal</b> field contains the command ID.

### -field szActionURL

Used only if eActionType<b></b> is <b>MMC_ACTION_LINK</b>.

[out] A pointer to a null-terminated string that contains the URL to which the task links. The URL must be fully qualified. The string can also contain a script instead of a URL.

### -field szScript

Used only if <b>eActionType</b> is <b>MMC_ACTION_SCRIPT</b>.

[out] A pointer to a null-terminated string that contains the script to run using the <a href="/previous-versions/hh869591(v=vs.85)">window.execScript</a> method on the taskpad DHTML page. To specify the script language, begin the string with the script language:

<ul>
<li>"VBSCRIPT:"</li>
<li>"JSCRIPT:"</li>
<li>"JAVASCRIPT:"</li>
</ul>
If no script language is specified, the default language is JavaScript.

## -remarks

Allocate the <b>szText</b>, <b>szHelpString</b>, <b>szActionURL</b>,and <b>szScript</b> strings used in the structure with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.

You should also allocate the strings in the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> or 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a> structure specified in the <b>sDisplayObject</b> member with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release them.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-ienumtask-next">IEnumTASK::Next</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a>



<a href="/windows/desktop/api/mmc/ne-mmc-mmc_action_type">MMC_ACTION_TYPE</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a>