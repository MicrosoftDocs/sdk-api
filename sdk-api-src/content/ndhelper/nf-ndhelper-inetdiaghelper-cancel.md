---
UID: NF:ndhelper.INetDiagHelper.Cancel
title: INetDiagHelper::Cancel
author: windows-driver-content
description: Cancels an ongoing diagnosis or repair.
old-location: ndf\inetdiaghelpe_cancel.htm
old-project: NDF
ms.assetid: 0df79e75-f3a6-43fd-82a3-2798ac1d99cd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Cancel, Cancel method [NDF], Cancel method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],Cancel method, INetDiagHelper.Cancel, INetDiagHelper::Cancel, ndf.inetdiaghelpe_cancel, ndhelper/INetDiagHelper::Cancel
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
req.typenames: REPAIR_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ndhelper.h
api_name:
-	INetDiagHelper.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetDiagHelper::Cancel


## -description


The <b>Cancel</b> method cancels an ongoing diagnosis or repair.


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



The <b>Cancel</b> method is required when building a Helper Class Extension.




## -see-also




<a href="https://msdn.microsoft.com/7f1b8a5b-389b-4276-a49d-94a39be3c35c">INetDiagHelper</a>
 

 

