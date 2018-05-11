---
UID: NN:mfidl.IMFTopoLoader
title: IMFTopoLoader
author: windows-driver-content
description: Converts a partial topology into a full topology.
old-location: mf\imftopoloader.htm
old-project: medfound
ms.assetid: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942, IMFTopoLoader, IMFTopoLoader interface [Media Foundation], IMFTopoLoader interface [Media Foundation],described, mf.imftopoloader, mfidl/IMFTopoLoader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopoLoader
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopoLoader interface


## -description


Converts a partial topology into a full topology. The topology loader exposes this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopoLoader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTopoLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopoLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ce47db-54a1-456a-a763-c62039aea2c9">Load</a>
</td>
<td align="left" width="63%">
Creates a fully loaded topology from the input partial topology.

</td>
</tr>
</table> 


## -remarks



To create the topology loader, call the <a href="https://msdn.microsoft.com/0c0173ef-9c29-465c-b725-ce38b220f94f">MFCreateTopoLoader</a> function.




## -see-also




<a href="https://msdn.microsoft.com/66aa07d8-6756-4d5b-9f0a-24b902da6fa2">Advanced Topology Building</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

