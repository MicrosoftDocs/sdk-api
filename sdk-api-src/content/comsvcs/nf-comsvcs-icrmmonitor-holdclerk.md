---
UID: NF:comsvcs.ICrmMonitor.HoldClerk
title: ICrmMonitor::HoldClerk
author: windows-sdk-content
description: Retrieves a pointer on the specified clerk.
old-location: cos\icrmmonitor_holdclerk.htm
old-project: cossdk
ms.assetid: 8e0f5197-d423-4b74-aaa1-2ec60e01d75c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: HoldClerk, HoldClerk method [COM+], HoldClerk method [COM+],ICrmMonitor interface, ICrmMonitor interface [COM+],HoldClerk method, ICrmMonitor.HoldClerk, ICrmMonitor::HoldClerk, _dtc_ICrmMonitor_HoldClerk, comsvcs/ICrmMonitor::HoldClerk, cos.icrmmonitor_holdclerk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitor.HoldClerk
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmMonitor::HoldClerk


## -description


Retrieves a pointer on the specified clerk.


## -parameters




### -param Index [in]

A <b>VARIANT</b> string containing the instance CLSID of the required CRM clerk.


### -param pItem [out]

A <b>VARIANT</b> <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer returning the interface to the specified CRM clerk.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_CLERKNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified CRM clerk was not found. It may have completed before it could be held.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ead5f782-8512-4387-b8f3-7be960f35bbe">ICrmMonitor</a>
 

 

