---
UID: NF:ndhelper.INetDiagHelper.Cleanup
title: INetDiagHelper::Cleanup
author: windows-sdk-content
description: Allows the Helper Class Extension to clean up resources following a diagnosis or repair operation.
old-location: ndf\inetdiaghelpe_cleanup.htm
tech.root: NDF
ms.assetid: d50d3415-8fa7-404c-8030-8ea7a59820e4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Cleanup, Cleanup method [NDF], Cleanup method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],Cleanup method, INetDiagHelper.Cleanup, INetDiagHelper::Cleanup, ndf.inetdiaghelpe_cleanup, ndhelper/INetDiagHelper::Cleanup
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
 - INetDiagHelper.Cleanup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetDiagHelper::Cleanup


## -description


The <b>Cleanup</b> method allows the Helper Class Extension to clean up resources following a diagnosis or repair operation. 


## -parameters






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



The <b>Cleanup</b> method is required when building a Helper Class Extension.




## -see-also




<a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a>
 

 

