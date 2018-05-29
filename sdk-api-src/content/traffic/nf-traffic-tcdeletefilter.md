---
UID: NF:traffic.TcDeleteFilter
title: TcDeleteFilter function
author: windows-sdk-content
description: The TcDeleteFilter function deletes a filter previously added with the TcAddFilter function.
old-location: qos\tcdeletefilter.htm
old-project: QOS
ms.assetid: 3a9eaffc-78d8-4473-a2d3-c060b104abd3
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: TcDeleteFilter, TcDeleteFilter function [QOS], _gqos_tcdeletefilter, qos.tcdeletefilter, traffic/TcDeleteFilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: traffic.h
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Traffic.dll
api_name:
-	TcDeleteFilter
product: Windows
targetos: Windows
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TcDeleteFilter function


## -description


The 
<b>TcDeleteFilter</b> function deletes a filter previously added with the 
<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a> function.


## -parameters




### -param FilterHandle [in]

Handle to the filter to be deleted, as received in a previous call to the 
<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a> function.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The filter handle is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Use of the 
<b>TcDeleteFilter</b> function requires administrative privilege.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c6d7c346-c353-4224-a8b5-56910e447902">TcAddFilter</a>
 

 

