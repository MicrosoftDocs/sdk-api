---
UID: NF:control.IAMStats.GetIndex
title: IAMStats::GetIndex
author: windows-sdk-content
description: The GetIndex method retrieves the index for a named statistic, or creates a new statistic.
old-location: dshow\iamstats_getindex.htm
old-project: DirectShow
ms.assetid: a5ea650c-42dd-405c-8ad9-6e48cf51353d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetIndex, GetIndex method [DirectShow], GetIndex method [DirectShow],IAMStats interface, IAMStats interface [DirectShow],GetIndex method, IAMStats.GetIndex, IAMStats::GetIndex, IAMStatsGetIndex, control/IAMStats::GetIndex, dshow.iamstats_getindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: WMPContextMenuInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStats.GetIndex
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IAMStats::GetIndex


## -description



The <code>GetIndex</code> method retrieves the index for a named statistic, or creates a new statistic.




## -parameters




### -param szName [in]

Specifies the name of the statistic.


### -param lCreate [in]

Specifies whether to create the statistic, if it is not defined already. If the value is <b>TRUE</b>, the method creates a new index for the statistic when it cannot find an existing entry with that name. If the value is <b>FALSE</b>, the method fails when the statistic does not already exist.


### -param plIndex [out]

Receives the index.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No match for this name.

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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd319776(v=VS.85).aspx">IAMStats Interface</a>
 

 

