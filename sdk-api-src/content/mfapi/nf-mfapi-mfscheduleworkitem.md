---
UID: NF:mfapi.MFScheduleWorkItem
title: MFScheduleWorkItem function
author: windows-sdk-content
description: Schedules an asynchronous operation to be completed after a specified interval.
old-location: mf\mfscheduleworkitem.htm
tech.root: medfound
ms.assetid: c14786e4-7fbe-4748-a6ba-e9e68f78b241
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFScheduleWorkItem, MFScheduleWorkItem function [Media Foundation], c14786e4-7fbe-4748-a6ba-e9e68f78b241, mf.mfscheduleworkitem, mfapi/MFScheduleWorkItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFScheduleWorkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFScheduleWorkItem function


## -description



Schedules an asynchronous operation to be completed after a specified interval.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface. The caller must implement this interface.


### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


### -param Timeout [in]

Time-out interval, in milliseconds. Set this parameter to a negative value. The callback is invoked after −<i>Timeout</i> milliseconds. For example, if <i>Timeout</i> is −5000, the callback is invoked after 5000 milliseconds.


### -param pKey [out]

Receives a key that can be used to cancel the timer. To cancel the timer, call <a href="https://msdn.microsoft.com/a24fae61-30c8-4aca-b067-22b99f904fd8">MFCancelWorkItem</a> and pass this key in the <i>Key</i> parameter.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



This function creates an asynchronous result object. When the timer interval elapses, the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method specified by <i>pCallback</i> is called.

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b698cae1-4f3b-4649-b6f7-583f223eb90c">MFScheduleWorkItemEx</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

