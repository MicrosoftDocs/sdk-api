---
UID: NF:ndhelper.INetDiagHelper.LowHealth
title: INetDiagHelper::LowHealth
author: windows-sdk-content
description: Check whether the component being diagnosed is healthy.
old-location: ndf\inetdiaghelpe_lowhealth.htm
tech.root: NDF
ms.assetid: 623de90f-c2dc-4879-9baf-4051d2d3691c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetDiagHelper interface [NDF],LowHealth method, INetDiagHelper.LowHealth, INetDiagHelper::LowHealth, LowHealth, LowHealth method [NDF], LowHealth method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_lowhealth, ndhelper/INetDiagHelper::LowHealth
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ndhelper.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelper.LowHealth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetDiagHelper::LowHealth


## -description


The <b>LowHealth</b> method enables the Helper Class Extension to check whether the component being diagnosed is healthy.


## -parameters




### -param pwszInstanceDescription [in]

A pointer to a null-terminated string containing the user-friendly description of the information being diagnosed.  For example, if a class were to diagnosis a connectivity issue with an IP address, the <i>pwszInstanceDescription</i> parameter would contain the host name.


### -param ppwszDescription [out]

A pointer to a null-terminated string containing the description of the issue found if the component is found to be unhealthy.


### -param pDeferredTime [out]

A pointer to the time, in seconds, to be deferred if the diagnosis cannot be started immediately.  This is used when the <i>pStatus</i> parameter is set to <b>DS_DEFERRED</b>.


### -param pStatus [out]

A pointer to the <a href="https://msdn.microsoft.com/2ad72ac5-3f33-4206-be39-1cfe11ee840d">DIAGNOSIS_STATUS</a> that is returned from the diagnosis.


## -returns



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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The diagnosis or repair operation has been canceled.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the failures encountered in the function.




## -remarks



The LowHealth method is required when building a Helper Class Extension.

If LowHealth returns <b>DS_CONFIRMED</b>, <i>ppwszDescription</i> will also contain a user-friendly description of the diagnosis result. The out parameter <i>pDeferredTime</i> contains the number of seconds this diagnosis needs to be deferred if pStatus returns <b>DS_DEFERRED</b>.

When LowHealth is confirmed, it may also optionally generate hypotheses in the <a href="https://msdn.microsoft.com/d17f5241-6efb-45a7-b355-8343e48b3261">GetLowerHypotheses</a> method for other helper classes if the problem may be caused by other components.  If not confirmed, NDF may further diagnose the problem by calling <a href="https://msdn.microsoft.com/4a555683-f7fd-43a4-808a-60579723293c">HighUtilization</a>.

LowHealth may also return <b>DS_INDETERMINATE</b> if it is unable to diagnose the problem, but cannot confirm that the component is healthy. In this case, NDF will treat it as <b>DS_CONFIRMED</b> if none of the other hypotheses are confirmed.




## -see-also




<a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a>
 

 

