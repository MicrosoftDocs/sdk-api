---
UID: NF:strmif.IGraphConfig.GetFilterFlags
title: IGraphConfig::GetFilterFlags
author: windows-sdk-content
description: The GetFilterFlags method retrieves a filter's configuration information.
old-location: dshow\igraphconfig_getfilterflags.htm
old-project: DirectShow
ms.assetid: 747c3865-1969-45e8-a2c9-dbd72a9ea463
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetFilterFlags, GetFilterFlags method [DirectShow], GetFilterFlags method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],GetFilterFlags method, IGraphConfig.GetFilterFlags, IGraphConfig::GetFilterFlags, IGraphConfigGetFilterFlags, dshow.igraphconfig_getfilterflags, strmif/IGraphConfig::GetFilterFlags
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
tech.root: 
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
-	IGraphConfig.GetFilterFlags
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphConfig::GetFilterFlags


## -description



The <code>GetFilterFlags</code> method retrieves a filter's configuration information.




## -parameters




### -param pFilter [in]

Pointer to the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface of a filter in the filter graph.


### -param pdwFlags [out]

Receives the current configuration flags.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
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
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The filter is not in the graph.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>



<a href="https://msdn.microsoft.com/1f2ed50e-8bb9-4076-ad0e-a7311acb8285">IGraphConfig::SetFilterFlags</a>
 

 

