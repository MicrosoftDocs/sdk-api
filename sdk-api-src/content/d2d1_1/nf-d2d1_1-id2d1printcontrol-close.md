---
UID: NF:d2d1_1.ID2D1PrintControl.Close
title: ID2D1PrintControl::Close (d2d1_1.h)
author: windows-sdk-content
description: Passes all remaining resources to the print sub-system, then clean up and close the current print job.
old-location: direct2d\id2d1printcontrol_close.htm
tech.root: Direct2D
ms.assetid: 2ADCA373-C461-4737-A292-AF29977B148C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [Direct2D], Close method [Direct2D],ID2D1PrintControl interface, ID2D1PrintControl interface [Direct2D],Close method, ID2D1PrintControl.Close, ID2D1PrintControl::Close, d2d1_1/ID2D1PrintControl::Close, direct2d.id2d1printcontrol_close
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1PrintControl.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PrintControl::Close


## -description


Passes all remaining resources to the print sub-system, then clean up and close the current print job. 


## -parameters






## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D2DERR_PRINT_JOB_CLOSED</td>
<td>The print job is already finished.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a>
 

 

