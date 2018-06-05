---
UID: NF:ndfapi.NdfCancelIncident
title: NdfCancelIncident function
author: windows-sdk-content
description: Used to cancel unneeded functions which have been previously called on an existing incident.
old-location: ndf\ndfcancelincident.htm
old-project: NDF
ms.assetid: dc0cbfc0-fcaa-44b2-a753-8df9f184b8ca
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NdfCancelIncident, NdfCancelIncident function [NDF], ndf.ndfcancelincident, ndfapi/NdfCancelIncident
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ndfapi.h
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
tech.root: 
req.typenames: UiInfo, *PUiInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ndfapi.dll
api_name:
-	NdfCancelIncident
product: Windows
targetos: Windows
req.lib: Ndfapi.lib
req.dll: Ndfapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdfCancelIncident function


## -description


The <b>NdfCancelIncident</b> function is used to cancel unneeded functions which have been previously called on an existing incident.


## -parameters




### -param Handle [in]

Type: <b>NDFHANDLE</b>

Handle to the Network Diagnostics Framework incident. This handle should match the handle of an existing incident.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
</table>
 

 Any result other than S_OK should be interpreted as an error.




## -remarks



Before using this API, an application must call an incident creation function such as <a href="https://msdn.microsoft.com/28ca2949-6867-4c9a-aebc-bf2a57627c04">NdfCreateWebIncident</a>.

<b>NdfCancelIncident</b> is primarily used to cancel calls to functions such as <a href="https://msdn.microsoft.com/69ae5624-7c3b-44a2-8468-d587739fc666">NdfDiagnoseIncident</a> or <a href="https://msdn.microsoft.com/570e7824-463f-4fc1-bc1a-16a1da31e8a3">NdfRepairIncident</a> which have been previously called, but are no longer needed. When <b>NdfCancelIncident</b> is called, NDF will stop the diagnosis/repair as soon as possible rather than calling the other functions (unless results have already been returned from those functions, in which case <b>NdfCancelIncident</b> will have no effect).


<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a> should be used to close an incident once it has been resolved, as <b>NdfCancelIncident</b> does not actually close the incident itself.



