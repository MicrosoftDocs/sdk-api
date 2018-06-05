---
UID: NN:xpsobjectmodel.IXpsOMPrintTicketResource
title: IXpsOMPrintTicketResource
author: windows-sdk-content
description: Provides an IStream interface to a PrintTicket resource.
old-location: xps\ixpsomprintticketresource.htm
old-project: printdocs
ms.assetid: 2f37dbd2-3078-4aa8-97e7-556a0ff2dd74
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMPrintTicketResource, IXpsOMPrintTicketResource interface [XPS Documents and Packaging], IXpsOMPrintTicketResource interface [XPS Documents and Packaging],described, xps.ixpsomprintticketresource, xpsobjectmodel/IXpsOMPrintTicketResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMPrintTicketResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPrintTicketResource interface


## -description


Provides an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface to a <b>PrintTicket</b> resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPrintTicketResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMPrintTicketResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPrintTicketResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0783cdda-84c6-4441-accf-10fc2610199b">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77e4af00-b2ed-4c88-80f1-fb3106ad1e75">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be  associated with this resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67d5ccfc-0f01-49d2-966e-09c7958921a5">IXpsOMObjectFactory::CreatePrintTicketResource</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

