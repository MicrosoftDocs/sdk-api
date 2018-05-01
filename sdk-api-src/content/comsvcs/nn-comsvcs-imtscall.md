---
UID: NN:comsvcs.IMTSCall
title: IMTSCall
author: windows-driver-content
description: Implements the batch work that is submitted through the activity created by the MTSCreateActivity function.
old-location: cos\imtscall.htm
old-project: cossdk
ms.assetid: dccf53c3-19d9-435b-91b7-98e41bd48e29
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IMTSCall, IMTSCall interface [COM+], IMTSCall interface [COM+], described, _cos_IMTSCall, comsvcs/IMTSCall, cos.imtscall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMTSCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMTSCall interface


## -description


<p class="CCE_Message">[<b>IMTSCall</b> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>.]

Implements the batch work that is submitted through the activity created by the <a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMTSCall</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMTSCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMTSCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/410ed66e-db55-41e6-8f09-df4fe3aad3f2">OnCall</a>
</td>
<td align="left" width="63%">
Triggers the execution of the batch work implemented in this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a45b29f0-d3f1-4593-9df5-4f6d617b93fa">IMTSActivity</a>



<a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>



<a href="https://msdn.microsoft.com/25ae1f2e-f937-4d06-9709-ded2fc8c5777">MTSCreateActivity</a>
 

 

