---
UID: NF:icontentprefetchertasktrigger.IContentPrefetcherTaskTrigger.TriggerContentPrefetcherTask
title: IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask (icontentprefetchertasktrigger.h)
description: Triggers a content prefetch background task for the specified app package.
helpviewer_keywords: ["IContentPrefetcherTaskTrigger interface [Web Services for Windows]","TriggerContentPrefetcherTask method","IContentPrefetcherTaskTrigger.TriggerContentPrefetcherTask","IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask","TriggerContentPrefetcherTask","TriggerContentPrefetcherTask method [Web Services for Windows]","TriggerContentPrefetcherTask method [Web Services for Windows]","IContentPrefetcherTaskTrigger interface","icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask","wsw.icontentprefetchertasktrigger_triggercontentprefetchertask"]
old-location: wsw\icontentprefetchertasktrigger_triggercontentprefetchertask.htm
tech.root: wsw
ms.assetid: F7AC2CA1-3726-4685-ABA8-5F9EE8FD54FF
ms.date: 12/05/2018
ms.keywords: IContentPrefetcherTaskTrigger interface [Web Services for Windows],TriggerContentPrefetcherTask method, IContentPrefetcherTaskTrigger.TriggerContentPrefetcherTask, IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask, TriggerContentPrefetcherTask, TriggerContentPrefetcherTask method [Web Services for Windows], TriggerContentPrefetcherTask method [Web Services for Windows],IContentPrefetcherTaskTrigger interface, icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask, wsw.icontentprefetchertasktrigger_triggercontentprefetchertask
req.header: icontentprefetchertasktrigger.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
 - IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask
 - icontentprefetchertasktrigger/IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IContentPrefetcherTaskTrigger.h
api_name:
 - IContentPrefetcherTaskTrigger.TriggerContentPrefetcherTask
---

# IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask


## -description

Triggers a content prefetch background task for the specified app package.

## -parameters

### -param packageFullName [in]

The package ID.

## -returns

Returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The provided package ID is not an installed package that has registered for the content prefetch background task, or the package ID is empty or null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The method call was not made at the required Medium Integrity Level (Medium IL).


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/icontentprefetchertasktrigger/nn-icontentprefetchertasktrigger-icontentprefetchertasktrigger">IContentPrefetcherTaskTrigger</a>