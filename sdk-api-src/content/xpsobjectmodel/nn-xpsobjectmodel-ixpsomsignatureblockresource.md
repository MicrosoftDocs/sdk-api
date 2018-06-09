---
UID: NN:xpsobjectmodel.IXpsOMSignatureBlockResource
title: IXpsOMSignatureBlockResource
author: windows-sdk-content
description: Provides an IStream interface to a signature block resource.
old-location: xps\ixpsomsignatureblockresource.htm
old-project: printdocs
ms.assetid: f5052470-487d-4f47-8d42-70538a4a45a8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMSignatureBlockResource, IXpsOMSignatureBlockResource interface [XPS Documents and Packaging], IXpsOMSignatureBlockResource interface [XPS Documents and Packaging],described, xps.ixpsomsignatureblockresource, xpsobjectmodel/IXpsOMSignatureBlockResource
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMSignatureBlockResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMSignatureBlockResource interface


## -description


Provides an IStream interface to a signature block resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMSignatureBlockResource</b> interface inherits from <a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>. <b>IXpsOMSignatureBlockResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMSignatureBlockResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b94e5b76-ae45-483c-b9ea-3987d7b4837a">GetOwner</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface that contains the resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e6c53fa-7180-454d-8bdc-332eb0d3fa27">GetStream</a>
</td>
<td align="left" width="63%">
Gets a new, read-only copy of the stream that is associated with this resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9a10907-9241-42af-8858-029c2cf925cf">SetContent</a>
</td>
<td align="left" width="63%">
Sets the read-only stream to be associated with this resource.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0948d495-f2da-4361-8365-d4316da72524">IXpsOMObjectFactory::CreateSignatureBlockResource</a>



<a href="https://msdn.microsoft.com/ed3d6ea0-efe5-4917-85fa-bd9ad1978b4e">IXpsOMResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

