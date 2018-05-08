---
UID: NF:strmif.IEnumFilters.Skip
title: IEnumFilters::Skip
author: windows-driver-content
description: The Skip method skips over a specified number of filters.
old-location: dshow\ienumfilters_skip.htm
old-project: DirectShow
ms.assetid: 594e25b1-03a8-4b6c-965c-f34dae9f3d3b
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IEnumFilters interface [DirectShow],Skip method, IEnumFilters.Skip, IEnumFilters::Skip, IEnumFiltersSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumFilters interface, dshow.ienumfilters_skip, strmif/IEnumFilters::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
-	IEnumFilters.Skip
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEnumFilters::Skip


## -description



The <code>Skip</code> method skips over a specified number of filters.




## -parameters




### -param cFilters






#### - cFilter [in]

Number of filters to skip.


## -returns



<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>S_FALSE</td>
<td>Skipped past the end of the sequence.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
<tr>
<td>VFW_E_ENUM_OUT_OF_SYNC</td>
<td>The graph has changed and is now inconsistent with the enumerator.</td>
</tr>
</table>
 




## -remarks



If the filter graph changes (for example, the application removes a filter), the enumerator is no longer be consistent with the graph, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://msdn.microsoft.com/997a6e56-cd11-42bf-b12c-a4418a4dc644">IEnumFilters::Reset</a> method. You can then call the <code>Skip</code> method safely.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e105ccff-86c6-45d5-aead-6d303d038e5a">IEnumFilters Interface</a>
 

 

