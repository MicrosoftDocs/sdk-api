---
UID: NN:shobjidl_core.IRunnableTask
title: IRunnableTask (shobjidl_core.h)
description: A free-threaded interface that can be exposed by an object to allow operations to be performed on a background thread.
helpviewer_keywords: ["IRunnableTask","IRunnableTask interface [Windows Shell]","IRunnableTask interface [Windows Shell]","described","_win32_IRunnableTask","shell.IRunnableTask","shobjidl_core/IRunnableTask"]
old-location: shell\IRunnableTask.htm
tech.root: shell
ms.assetid: 158a6688-949b-4075-a790-fd6efb88792c
ms.date: 12/05/2018
ms.keywords: IRunnableTask, IRunnableTask interface [Windows Shell], IRunnableTask interface [Windows Shell],described, _win32_IRunnableTask, shell.IRunnableTask, shobjidl_core/IRunnableTask
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunnableTask
 - shobjidl_core/IRunnableTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRunnableTask
---

# IRunnableTask interface


## -description

A free-threaded interface that can be exposed by an object to allow operations to be performed on a background thread. For example, if the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation">IExtractImage::GetLocation</a> method returns E_PENDING, the calling application is permitted to extract the image on a background thread.

## -inheritance

The <b>IRunnableTask</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRunnableTask</b> also has these types of members:

## -remarks

Implement <b>IRunnableTask</b> if your namespace extension is free-threaded, and you want to allow a task such as icon extraction to be managed by a scheduler. Only the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-run">Run</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-isrunning">IsRunning</a> methods must be implemented. If you do not want to implement <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-kill">Kill</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-resume">Resume</a>, and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-suspend">Suspend</a>, simply have them return E_NOTIMPL.

If you are using <b>IRunnableTask</b> to extract an image on a background thread, that is, if the object exposes <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage">IExtractImage</a>, then <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-run">Run</a> is not necessary, as the system will use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-extract">IExtractImage::Extract</a> to manage the task. The other methods (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-kill">Kill</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-resume">Resume</a>, and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-suspend">Suspend</a>) are optional in this case, but will be used by the system if they are implemented.

You do not call this interface directly. <b>IRunnableTask</b> is used by the operating system only when it has confirmed that your application is aware of this interface.

<b>IRunnableTask</b> implements <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> as well as the five listed methods.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>
