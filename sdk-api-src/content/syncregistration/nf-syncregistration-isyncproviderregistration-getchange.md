---
UID: NF:syncregistration.ISyncProviderRegistration.GetChange
title: ISyncProviderRegistration::GetChange (syncregistration.h)
description: Gets an ISyncRegistrationChange object that represents a new registration event.
helpviewer_keywords: ["GetChange","GetChange method [Windows Sync]","GetChange method [Windows Sync]","ISyncProviderRegistration interface","ISyncProviderRegistration interface [Windows Sync]","GetChange method","ISyncProviderRegistration.GetChange","ISyncProviderRegistration::GetChange","syncregistration/ISyncProviderRegistration::GetChange","winsync.isyncproviderregistration_getchange"]
old-location: winsync\isyncproviderregistration_getchange.htm
tech.root: winsync
ms.assetid: 6a65ba8b-b9cb-4d8c-8d18-9627547f9982
ms.date: 12/05/2018
ms.keywords: GetChange, GetChange method [Windows Sync], GetChange method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetChange method, ISyncProviderRegistration.GetChange, ISyncProviderRegistration::GetChange, syncregistration/ISyncProviderRegistration::GetChange, winsync.isyncproviderregistration_getchange
req.header: syncregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - ISyncProviderRegistration::GetChange
 - syncregistration/ISyncProviderRegistration::GetChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.GetChange
---

# ISyncProviderRegistration::GetChange


## -description

	Gets an <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncregistrationchange">ISyncRegistrationChange</a> object that represents a new registration event.

## -parameters

### -param hEvent [in]

A <b>HANDLE</b> returned by the <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-registerforevent">RegisterForEvent</a> method.

### -param ppChange [out]

The <a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncregistrationchange">ISyncRegistrationChange</a> object
    that contains the event, and the ID of the synchronization provider or synchronization provider configuration UI that has changed.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
All outstanding events have been retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

This method resets the event that is passed in so that it will be set on a subsequent change in the registration store.  In order to retrieve all events from the store, this method should be called until <b>S_FALSE</b> is returned and <i>ppChange</i> is <b>NULL</b>.

This method returns the changes that have occurred since <a href="/previous-versions/windows/desktop/api/syncregistration/nf-syncregistration-isyncproviderregistration-registerforevent">RegisterForEvent</a> or <b>GetChange</b> (whichever happened last) was last called for the given <b>HANDLE</b>.  This means that if multiple changes are made to an item before <b>GetChange</b> can be called, these changes will be represented as a single change object returned from <b>GetChange</b>.  In the case of an item being registered and unregistered between calls, no change will be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/syncregistration/nn-syncregistration-isyncproviderregistration">ISyncProviderRegistration Interface</a>