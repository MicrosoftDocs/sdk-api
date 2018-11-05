---
UID: NN:shobjidl_core.IRunnableTask
title: IRunnableTask
author: windows-sdk-content
description: A free-threaded interface that can be exposed by an object to allow operations to be performed on a background thread.
old-location: shell\IRunnableTask.htm
tech.root: shell
ms.assetid: 158a6688-949b-4075-a790-fd6efb88792c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IRunnableTask, IRunnableTask interface [Windows Shell], IRunnableTask interface [Windows Shell],described, _win32_IRunnableTask, shell.IRunnableTask, shobjidl_core/IRunnableTask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRunnableTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunnableTask interface


## -description


A free-threaded interface that can be exposed by an object to allow operations to be performed on a background thread. For example, if the <a href="https://msdn.microsoft.com/f1113429-ea89-4650-b345-db9e275232e6">IExtractImage::GetLocation</a> method returns E_PENDING, the calling application is permitted to extract the image on a background thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunnableTask</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRunnableTask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRunnableTask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14117a47-d462-4be1-b440-8d422c938815">IsRunning</a>
</td>
<td align="left" width="63%">
Requests information on the state of a task, such as thumbnail extraction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7465aded-43ff-4b63-8a90-b9f55240625b">Kill</a>
</td>
<td align="left" width="63%">
Requests that a task be stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51ff7ae2-b2db-4eee-b03b-da46ff0ec901">Resume</a>
</td>
<td align="left" width="63%">
Requests that a task resume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b929543c-d5b3-4d48-b13f-bbef568287a5">Run</a>
</td>
<td align="left" width="63%">
Requests that a task begin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f376d8e7-65d2-4824-a20f-e8604295df3f">Suspend</a>
</td>
<td align="left" width="63%">
Requests that a task be suspended.

</td>
</tr>
</table> 


## -remarks



Implement <b>IRunnableTask</b> if your namespace extension is free-threaded, and you want to allow a task such as icon extraction to be managed by a scheduler. Only the <a href="https://msdn.microsoft.com/b929543c-d5b3-4d48-b13f-bbef568287a5">Run</a> and <a href="https://msdn.microsoft.com/14117a47-d462-4be1-b440-8d422c938815">IsRunning</a> methods must be implemented. If you do not want to implement <a href="https://msdn.microsoft.com/7465aded-43ff-4b63-8a90-b9f55240625b">Kill</a>, <a href="https://msdn.microsoft.com/51ff7ae2-b2db-4eee-b03b-da46ff0ec901">Resume</a>, and <a href="https://msdn.microsoft.com/f376d8e7-65d2-4824-a20f-e8604295df3f">Suspend</a>, simply have them return E_NOTIMPL.

If you are using <b>IRunnableTask</b> to extract an image on a background thread, that is, if the object exposes <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a>, then <a href="https://msdn.microsoft.com/b929543c-d5b3-4d48-b13f-bbef568287a5">Run</a> is not necessary, as the system will use <a href="https://msdn.microsoft.com/7c40e2cf-c706-4a4a-819f-a416d6846158">IExtractImage::Extract</a> to manage the task. The other methods (<a href="https://msdn.microsoft.com/7465aded-43ff-4b63-8a90-b9f55240625b">Kill</a>, <a href="https://msdn.microsoft.com/51ff7ae2-b2db-4eee-b03b-da46ff0ec901">Resume</a>, and <a href="https://msdn.microsoft.com/f376d8e7-65d2-4824-a20f-e8604295df3f">Suspend</a>) are optional in this case, but will be used by the system if they are implemented.

You do not call this interface directly. <b>IRunnableTask</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<b>IRunnableTask</b> implements <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> as well as the five listed methods.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


