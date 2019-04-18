---
UID: NF:msctf.ITfPropertyStore.Shrink
title: ITfPropertyStore::Shrink (msctf.h)
author: windows-sdk-content
description: ITfPropertyStore::Shrink method
old-location: tsf\itfpropertystore_shrink.htm
tech.root: TSF
ms.assetid: 55637d69-2f1a-435d-be23-4c29ec57b2ea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfPropertyStore interface [Text Services Framework],Shrink method, ITfPropertyStore.Shrink, ITfPropertyStore::Shrink, Shrink, Shrink method [Text Services Framework], Shrink method [Text Services Framework],ITfPropertyStore interface, _tsf_itfpropertystore_shrink_ref, msctf/ITfPropertyStore::Shrink, tsf.itfpropertystore_shrink
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfPropertyStore.Shrink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfPropertyStore::Shrink


## -description




## -parameters




### -param pRangeNew [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the truncated range.


### -param pfFree [out]

Pointer to a <b>BOOL</b> variable that receives a value that indicates if the property store should be retained. Receives a nonzero value if the property store should be retained or zero if the property store should be discarded. If the property store is discarded, the TSF manager will set the property value to VT_EMPTY and release the property store.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



If this method returns a value other than S_OK, the property store is discarded.




## -see-also




<a href="https://msdn.microsoft.com/0678e622-3733-499b-b289-c8c181d4638c">ITfPropertyStore</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

