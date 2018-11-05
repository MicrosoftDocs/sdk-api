---
UID: NF:comsvcs.ICrmMonitorClerks.ActivityId
title: ICrmMonitorClerks::ActivityId
author: windows-sdk-content
description: Retrieves the activity ID of the CRM Worker for the specified index.
old-location: cos\icrmmonitorclerks_activityid.htm
tech.root: cossdk
ms.assetid: 19a242a6-ce21-4ce5-984e-cc2220476e2b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ActivityId, ActivityId method [COM+], ActivityId method [COM+],ICrmMonitorClerks interface, ICrmMonitorClerks interface [COM+],ActivityId method, ICrmMonitorClerks.ActivityId, ICrmMonitorClerks::ActivityId, _dtc_ICrmMonitorClerks_ActivityId, comsvcs/ICrmMonitorClerks::ActivityId, cos.icrmmonitorclerks_activityid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.ActivityId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmMonitorClerks::ActivityId


## -description


Retrieves the activity ID of the CRM Worker for the specified index.


## -parameters




### -param Index [in]

The index of the required CRM clerk as a numeric <b>Variant</b>, or the instance CLSID as a <b>Variant</b> string.


### -param pItem [out]

The activity ID of the CRM Worker.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684207(v=VS.85).aspx">ICrmMonitorClerks</a>
 

 

