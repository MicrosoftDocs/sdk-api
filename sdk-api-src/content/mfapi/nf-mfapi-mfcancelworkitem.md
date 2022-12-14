---
UID: NF:mfapi.MFCancelWorkItem
title: MFCancelWorkItem function (mfapi.h)
description: Attempts to cancel an asynchronous operation that was scheduled with MFScheduleWorkItem or MFScheduleWorkItemEx.
helpviewer_keywords: ["MFCancelWorkItem","MFCancelWorkItem function [Media Foundation]","a24fae61-30c8-4aca-b067-22b99f904fd8","mf.mfcancelworkitem","mfapi/MFCancelWorkItem"]
old-location: mf\mfcancelworkitem.htm
tech.root: mf
ms.assetid: a24fae61-30c8-4aca-b067-22b99f904fd8
ms.date: 12/05/2018
ms.keywords: MFCancelWorkItem, MFCancelWorkItem function [Media Foundation], a24fae61-30c8-4aca-b067-22b99f904fd8, mf.mfcancelworkitem, mfapi/MFCancelWorkItem
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCancelWorkItem
 - mfapi/MFCancelWorkItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCancelWorkItem
---

# MFCancelWorkItem function


## -description

Attempts to cancel an asynchronous operation that was scheduled with <a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem">MFScheduleWorkItem</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex">MFScheduleWorkItemEx</a>.

## -parameters

### -param Key [in]

The key that was received in the <i>pKey</i> parameter of the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem">MFScheduleWorkItem</a>, <a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex">MFScheduleWorkItemEx</a>, or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem">MFPutWaitingWorkItem</a> functions.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Because work items are asynchronous, the  work-item callback might still be invoked after <b>MFCancelWorkItem</b> is called.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>