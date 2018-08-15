---
UID: NF:ndhelper.INetDiagHelper.HighUtilization
title: INetDiagHelper::HighUtilization
author: windows-sdk-content
description: Check whether the corresponding component is highly utilized.
old-location: ndf\inetdiaghelpe_highutilization.htm
old-project: ndf
ms.assetid: 4a555683-f7fd-43a4-808a-60579723293c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HighUtilization, HighUtilization method [NDF], HighUtilization method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],HighUtilization method, INetDiagHelper.HighUtilization, INetDiagHelper::HighUtilization, ndf.inetdiaghelpe_highutilization, ndhelper/INetDiagHelper::HighUtilization
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ndhelper.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: REPAIR_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelper.HighUtilization
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetDiagHelper::HighUtilization


## -description


The <b>HighUtilization</b> method enables the Helper Class Extension to check whether the corresponding component is highly utilized.


## -parameters




### -param pwszInstanceDescription [in]

A pointer to a null-terminated string containing the user-friendly description of the information being diagnosed.  For example, if a class were to diagnosis a connectivity issue with an IP address, the <i>pwszInstanceDescription</i> parameter would contain the host name.


### -param ppwszDescription [out]

A pointer to a null-terminated string containing the description of high utilization diagnosis result.


### -param pDeferredTime [out]

A pointer to the time, in seconds, to be deferred if the diagnosis cannot be started immediately. This is used when the <i>pStatus</i> parameter is set to <b>DS_DEFERRED</b>.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This optional method is not implemented.

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



This method is not required when building a Helper Class Extension.




## -see-also




<a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a>
 

 

