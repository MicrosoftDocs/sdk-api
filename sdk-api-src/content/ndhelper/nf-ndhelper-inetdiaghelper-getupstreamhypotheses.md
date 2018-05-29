---
UID: NF:ndhelper.INetDiagHelper.GetUpStreamHypotheses
title: INetDiagHelper::GetUpStreamHypotheses
author: windows-sdk-content
description: Generate hypotheses for possible causes of high utilization in the upstream network components.
old-location: ndf\inetdiaghelpe_getupstreathypotheses.htm
old-project: NDF
ms.assetid: e683a2eb-8dec-47e2-ae3d-6c12a9b2773d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetUpStreamHypotheses, GetUpStreamHypotheses method [NDF], GetUpStreamHypotheses method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetUpStreamHypotheses method, INetDiagHelper.GetUpStreamHypotheses, INetDiagHelper::GetUpStreamHypotheses, ndf.inetdiaghelpe_getupstreathypotheses, ndhelper/INetDiagHelper::GetUpStreamHypotheses
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: REPAIR_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ndhelper.h
api_name:
-	INetDiagHelper.GetUpStreamHypotheses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetDiagHelper::GetUpStreamHypotheses


## -description


The <b>GetUpStreamHypotheses</b> method asks the Helper Class Extension to generate hypotheses for possible causes of high utilization in the upstream network components that depend on it.


## -parameters




### -param pcelt [out]

A pointer to a count of elements in the <b>HYPOTHESIS</b> array.


### -param pprgHypotheses [out]

A pointer to a <a href="https://msdn.microsoft.com/8f137633-8501-404c-9540-d558be9beeca">HYPOTHESIS</a> array.


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
 

 

