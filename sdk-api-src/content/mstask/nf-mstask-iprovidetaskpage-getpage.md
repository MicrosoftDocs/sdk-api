---
UID: NF:mstask.IProvideTaskPage.GetPage
title: IProvideTaskPage::GetPage (mstask.h)
description: This method retrieves one or more property sheet pages associated with a task object.
helpviewer_keywords: ["GetPage","GetPage method [Task Scheduler]","GetPage method [Task Scheduler]","IProvideTaskPage interface","IProvideTaskPage interface [Task Scheduler]","GetPage method","IProvideTaskPage.GetPage","IProvideTaskPage::GetPage","_msb_iprovidetaskpage_getpage","mstask/IProvideTaskPage::GetPage","taskschd.iprovidetaskpage_getpage"]
old-location: taskschd\iprovidetaskpage_getpage.htm
tech.root: taskschd
ms.assetid: 2313abc1-587f-473b-8d2e-390dfa7234ab
ms.date: 12/05/2018
ms.keywords: GetPage, GetPage method [Task Scheduler], GetPage method [Task Scheduler],IProvideTaskPage interface, IProvideTaskPage interface [Task Scheduler],GetPage method, IProvideTaskPage.GetPage, IProvideTaskPage::GetPage, _msb_iprovidetaskpage_getpage, mstask/IProvideTaskPage::GetPage, taskschd.iprovidetaskpage_getpage
req.header: mstask.h
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IProvideTaskPage::GetPage
 - mstask/IProvideTaskPage::GetPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IProvideTaskPage.GetPage
---

# IProvideTaskPage::GetPage


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves one or more property sheet pages associated with a task object.

## -parameters

### -param tpType [in]

One of the following 
<a href="/windows/desktop/api/mstask/ne-mstask-taskpage">TASKPAGE</a> enumeration values that specify the page to return. 







#### TASKPAGE_TASK

General page property.



#### TASKPAGE_SCHEDULE

Schedule properties for the task.



#### TASKPAGE_SETTINGS

Settings properties for the task.

### -param fPersistChanges [in]

Specifies whether changes to the task object are made persistent automatically. If <b>TRUE</b>, the page updates the persistent task object automatically if there is a change made on release. If <b>FALSE</b>, the caller is responsible for making task object changes persistent by calling <b>IPersistFile::Save</b> on the task object.

### -param phPage [out]

Handle to the returned property sheet page of the task object. This handle can then be used to display the page.

## -returns

Returns S_OK if the method was successful, or STG_E_NOTFILEBASEDSTORAGE if the task has not been saved to disk.

## -remarks

To retrieve the 
<a href="/windows/desktop/api/mstask/nn-mstask-iprovidetaskpage">IProvideTaskPage</a> interface, call <b>ITask::QueryInterface</b>.

The following code shows the variable declaration and calling syntax for using this method and for calling <b>ITask::QueryInterface</b>.


#### Examples

For a complete example of retrieving and displaying the general task page of a known task, see <a href="/windows/desktop/TaskSchd/retrieving-a-task-page-example">Retrieving a Task Page Example</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-iprovidetaskpage">IProvideTaskPage</a>



<a href="/windows/desktop/api/mstask/ne-mstask-taskpage">TASKPAGE</a>