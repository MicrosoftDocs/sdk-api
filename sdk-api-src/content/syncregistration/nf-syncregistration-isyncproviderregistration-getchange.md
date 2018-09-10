---
UID: NF:syncregistration.ISyncProviderRegistration.GetChange
title: ISyncProviderRegistration::GetChange
author: windows-sdk-content
description: Gets an ISyncRegistrationChange object that represents a new registration event.
old-location: winsync\isyncproviderregistration_getchange.htm
tech.root: winsync
ms.assetid: 6a65ba8b-b9cb-4d8c-8d18-9627547f9982
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetChange, GetChange method [Windows Sync], GetChange method [Windows Sync],ISyncProviderRegistration interface, ISyncProviderRegistration interface [Windows Sync],GetChange method, ISyncProviderRegistration.GetChange, ISyncProviderRegistration::GetChange, syncregistration/ISyncProviderRegistration::GetChange, winsync.isyncproviderregistration_getchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncregistration.h
api_name:
 - ISyncProviderRegistration.GetChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncProviderRegistration::GetChange


## -description


	Gets an <a href="https://msdn.microsoft.com/45376bd2-1f5f-4f4c-9c4c-f5add9438d5c">ISyncRegistrationChange</a> object that represents a new registration event.


## -parameters




### -param hEvent [in]

A <b>HANDLE</b> returned by the <a href="https://msdn.microsoft.com/b636a3b4-2ac2-4400-b8ed-4430f598db7b">RegisterForEvent</a> method.


### -param ppChange [out]

The <a href="https://msdn.microsoft.com/45376bd2-1f5f-4f4c-9c4c-f5add9438d5c">ISyncRegistrationChange</a> object
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

This method returns the changes that have occurred since <a href="https://msdn.microsoft.com/b636a3b4-2ac2-4400-b8ed-4430f598db7b">RegisterForEvent</a> or <b>GetChange</b> (whichever happened last) was last called for the given <b>HANDLE</b>.  This means that if multiple changes are made to an item before <b>GetChange</b> can be called, these changes will be represented as a single change object returned from <b>GetChange</b>.  In the case of an item being registered and unregistered between calls, no change will be returned.




## -see-also




<a href="https://msdn.microsoft.com/e7cf0c05-9d07-4630-ae34-9a9dd81492b2">ISyncProviderRegistration Interface</a>
 

 

