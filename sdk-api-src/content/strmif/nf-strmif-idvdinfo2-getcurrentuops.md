---
UID: NF:strmif.IDvdInfo2.GetCurrentUOPS
title: IDvdInfo2::GetCurrentUOPS
author: windows-sdk-content
description: The GetCurrentUOPS method retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.
old-location: dshow\idvdinfo2_getcurrentuops.htm
old-project: DirectShow
ms.assetid: 71ae88f0-17ad-4530-b2e7-6a8155c14a97
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetCurrentUOPS, GetCurrentUOPS method [DirectShow], GetCurrentUOPS method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentUOPS method, IDvdInfo2.GetCurrentUOPS, IDvdInfo2::GetCurrentUOPS, IDvdInfo2GetCurrentUOPS, dshow.idvdinfo2_getcurrentuops, strmif/IDvdInfo2::GetCurrentUOPS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetCurrentUOPS
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetCurrentUOPS


## -description



The <code>GetCurrentUOPS</code> method retrieves a set of flags indicating which navigation commands, if any, the content authors have explicitly disabled for the current disc location.




## -parameters




### -param pulUOPs [out]

Receives a bitwise <b>OR</b> of <a href="https://msdn.microsoft.com/419d3d5f-e775-438e-9754-0291df6a1ed7">VALID_UOP_FLAG</a> values. Each bit represents the state (valid or not valid) of a user operation (UOP). If the bit is set, then that user operation is prohibited. See Remarks.


## -returns



Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pulUOPs</i> is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



DVD authors can insert UOP commands at almost any place on the disc to disallow a navigation command that would otherwise be permitted within the current DVD domain. In other words, UOP commands enable disc authors to override the usual navigation permissions.

A DVD player application should normally never have to use this method because the DVD Navigator automatically checks all UOP permissions before proceeding with any command, and will return VFW_E_DVD_OPERATION_INHIBITED from any method if the command is invalid under the current UOP. If your application needs to track the current UOP permissions itself, you can call <code>GetCurrentUOPS</code> whenever the current UOP permissions are required, or you can handle the <a href="https://msdn.microsoft.com/dfe698b9-abe5-44a7-9844-f408f11fd0ce">EC_DVD_VALID_UOPS_CHANGE</a> event notification in your message loop and retrieve the UOP information from the <i>lParam1</i> parameter. The latter approach is generally more efficient.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

