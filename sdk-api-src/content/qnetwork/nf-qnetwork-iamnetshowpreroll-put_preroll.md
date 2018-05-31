---
UID: NF:qnetwork.IAMNetShowPreroll.put_Preroll
title: IAMNetShowPreroll::put_Preroll
author: windows-sdk-content
description: The put_Preroll method specifies whether the filter should start prerolling.
old-location: dshow\iamnetshowpreroll_put_preroll.htm
old-project: DirectShow
ms.assetid: 3296f0ab-2be8-4693-99bd-5dae0672df26
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMNetShowPreroll interface [DirectShow],put_Preroll method, IAMNetShowPreroll.put_Preroll, IAMNetShowPreroll::put_Preroll, IAMNetShowPrerollput_Preroll, dshow.iamnetshowpreroll_put_preroll, put_Preroll, put_Preroll method [DirectShow], put_Preroll method [DirectShow],IAMNetShowPreroll interface, qnetwork/IAMNetShowPreroll::put_Preroll
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: qnetwork.h
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetShowPreroll.put_Preroll
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMNetShowPreroll::put_Preroll


## -description



The <code>put_Preroll</code> method specifies whether the filter should start prerolling.




## -parameters




### -param fPreroll

Specifies one of the following values:

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
<td>VARIANT_TRUE</td>
<td>Begin prerolling.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Stop prerolling.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/13478678-00de-48e6-b9e7-fd47db423290">IAMNetShowPreroll Interface</a>
 

 

