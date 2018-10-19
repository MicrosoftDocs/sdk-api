---
UID: NF:textstor.IAnchor.ClearChangeHistory
title: IAnchor::ClearChangeHistory
author: windows-sdk-content
description: The IAnchor::ClearChangeHistory method clears the anchor change history flags.
old-location: tsf\ianchor_clearchangehistory.htm
tech.root: TSF
ms.assetid: 3780ab3d-6b77-45bc-9630-747fa5caaecc
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ClearChangeHistory, ClearChangeHistory method [Text Services Framework], ClearChangeHistory method [Text Services Framework],IAnchor interface, IAnchor interface [Text Services Framework],ClearChangeHistory method, IAnchor.ClearChangeHistory, IAnchor::ClearChangeHistory, textstor/IAnchor::ClearChangeHistory, tsf.ianchor_clearchangehistory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - Msctf.dll
api_name:
 - IAnchor.ClearChangeHistory
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IAnchor::ClearChangeHistory


## -description


The <b>IAnchor::ClearChangeHistory</b> method clears the anchor change history flags.


## -parameters






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



Applications should clear the anchor change history flags after receiving this call. The change history flags were set by <a href="https://msdn.microsoft.com/d373a379-1d27-4438-abaf-2e11f2332790">IAnchor::GetChangeHistory</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/d373a379-1d27-4438-abaf-2e11f2332790">IAnchor::GetChangeHistory
      </a>
 

 

