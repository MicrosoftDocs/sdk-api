---
UID: NF:strmif.IGraphConfig.GetStartTime
title: IGraphConfig::GetStartTime (strmif.h)
author: windows-sdk-content
description: The GetStartTime method retrieves the reference time that was used when the filter graph was last put into a running state.
old-location: dshow\igraphconfig_getstarttime.htm
tech.root: DirectShow
ms.assetid: 76d06517-3029-4ece-934e-b1c6f7f65f2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStartTime, GetStartTime method [DirectShow], GetStartTime method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],GetStartTime method, IGraphConfig.GetStartTime, IGraphConfig::GetStartTime, IGraphConfigGetStartTime, dshow.igraphconfig_getstarttime, strmif/IGraphConfig::GetStartTime
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
 - IGraphConfig.GetStartTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGraphConfig::GetStartTime


## -description



The <code>GetStartTime</code> method retrieves the reference time that was used when the filter graph was last put into a running state.




## -parameters




### -param prtStart [out]

Receives the start time.


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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter graph is not in a running state.

</td>
</tr>
</table>
 




## -remarks



The filter graph must currently be in a running state or this method will fail.



