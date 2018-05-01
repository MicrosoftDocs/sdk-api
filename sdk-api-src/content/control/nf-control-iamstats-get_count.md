---
UID: NF:control.IAMStats.get_Count
title: IAMStats::get_Count method
author: windows-driver-content
description: The get_Count method retrieves the number of statistics.
old-location: dshow\iamstats_get_count.htm
old-project: DirectShow
ms.assetid: 48f2543a-7c93-4d4f-a568-b8066e9545fd
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMStats, IAMStats interface [DirectShow], get_Count method, IAMStats::get_Count, IAMStatsget_Count, control/IAMStats::get_Count, dshow.iamstats_get_count, get_Count method [DirectShow], get_Count method [DirectShow], IAMStats interface, get_Count,IAMStats.get_Count
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
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
req.typenames: WMPContextMenuInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMStats.get_Count
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMStats::get_Count method


## -description



The <code>get_Count</code> method retrieves the number of statistics.




## -parameters




### -param plCount [out]

Receives the number of statistics.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/01dbaba2-fdca-4f42-8816-fd99c4364dbd">IAMStats Interface</a>
 

 

