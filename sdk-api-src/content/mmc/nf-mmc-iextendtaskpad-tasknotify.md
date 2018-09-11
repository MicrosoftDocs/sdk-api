---
UID: NF:mmc.IExtendTaskPad.TaskNotify
title: IExtendTaskPad::TaskNotify
author: windows-sdk-content
description: The IExtendTaskPad::TaskNotify method enables MMC to notify the snap-in when a task is extended. If the taskpad is a list-view taskpad, MMC also calls IExtendTaskPad::TaskNotify when a list-view button is extended.
old-location: mmc\iextendtaskpad_tasknotify.htm
tech.root: mmc
ms.assetid: c20d87f9-a5a0-41b9-b343-a11e8b41ed71
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IExtendTaskPad interface [MMC],TaskNotify method, IExtendTaskPad.TaskNotify, IExtendTaskPad::TaskNotify, TaskNotify, TaskNotify method [MMC], TaskNotify method [MMC],IExtendTaskPad interface, _slate_iextendtaskpad_tasknotify, mmc.iextendtaskpad_tasknotify, mmc/IExtendTaskPad::TaskNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendTaskPad.TaskNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExtendTaskPad::TaskNotify


## -description


The <b>IExtendTaskPad::TaskNotify</b> method enables MMC to notify the snap-in when a task is extended. If the taskpad is a list-view taskpad, MMC also calls <b>IExtendTaskPad::TaskNotify</b> when a list-view button is extended.


## -parameters




### -param pdo [in]

A pointer to the data object for the scope item that owns the taskpad. If your snap-in owns the item that displays the taskpad, pdo is a pointer to that item. If your snap-in is extending the taskpad of another snap-in, pdo is a pointer to the item in the snap-in that owns the taskpad.


### -param arg [in]

A pointer to a VARIANT structure that contains information passed back from the CIC control on the taskpad.

Taskpads using MMC taskpad templates

For the MMC-supplied taskpads, the VARIANT structure contains the command ID for the taskpad task or list-view button that was ed.

The vt field is VT_I4 and the lVal field contains the command ID for the taskpad task or list-view button that was ed. List-view buttons apply only to list-view taskpads.

A task command ID is specified in the nCommandID member of the 
<a href="https://msdn.microsoft.com/bb101c09-947f-4316-890a-86e09358d88c">MMC_TASK</a> structure, which is passed in the <a href="https://msdn.microsoft.com/cb568307-7172-4941-a888-ff059f5256b6">IEnumTASK::Next</a> method that MMC calls when it retrieves the information for that task during the setup of the taskpad.

A list-view button is the button specified in the szButtonText member of the 
<a href="https://msdn.microsoft.com/53e3cd8f-9d78-4edc-a0bb-3b409857561f">MMC_LISTPAD_INFO</a> structure, which is passed in the <a href="https://msdn.microsoft.com/73e9d281-9bf9-4a50-b3e8-226ed3593f7a">IExtendTaskPad::GetListPadInfo</a> method that MMC calls when it is setting up the list-view taskpad. The list-view button command ID is specified in the nCommandID member of 
MMC_LISTPAD_INFO.

Taskpads using custom HTML pages

For custom taskpads, the VARIANT structure can contain any data that the script on the custom HTML page wants to pass through the CIC object 
TaskNotify method


### -param param [in]

A pointer to a VARIANT structure that contains information passed back from the CIC control on the taskpad.

Taskpads that use the MMC taskpad templates ignore this parameter. However, custom taskpads can use it to pass an additional value back to the snap-in.


## -returns



This method can return one of these values.




## -remarks



The snap-in can identify the scope item that owns the taskpad using the pdo pointer; it then can identify the task by the VARIANT value returned in the arg parameter. If the taskpad is a list-view taskpad, the snap-in can identify the selected item (or items if multiselection is supported) in a result list using the 
<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a> interface. Based on this data, the snap-in can perform the appropriate actions on the appropriate object.

If a taskpad list-view button is ed for a list-view taskpad, the snap-in can identify the button for the particular taskpad by the VARIANT value returned in the arg parameter.

A custom taskpad can pass any values that it determines should be sent in the arg and param parameters.




## -see-also




<a href="https://msdn.microsoft.com/7cf1ff4f-bd45-4ead-a005-e0f38aed9039">IEnumTASK</a>



<a href="https://msdn.microsoft.com/30f5b526-d2d5-48a6-be5f-d0f2ba9397c4">IExtendTaskPad</a>
 

 

