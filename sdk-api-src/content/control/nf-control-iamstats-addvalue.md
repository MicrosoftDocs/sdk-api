---
UID: NF:control.IAMStats.AddValue
title: IAMStats::AddValue
author: windows-sdk-content
description: The AddValue method records a new value.
old-location: dshow\iamstats_addvalue.htm
tech.root: DirectShow
ms.assetid: a408b106-702c-4ecc-a424-b4b3588ea58f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddValue, AddValue method [DirectShow], AddValue method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],AddValue method, IAMStats.AddValue, IAMStats::AddValue, IAMStatsAddValue, control/IAMStats::AddValue, dshow.iamstats_addvalue
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStats.AddValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStats::AddValue


## -description



The <code>AddValue</code> method records a new value.




## -parameters




### -param lIndex [in]

Specifies the index of the statistic.


### -param dValue [in]

Specifies the value to record.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/01dbaba2-fdca-4f42-8816-fd99c4364dbd">IAMStats Interface</a>
 

 

