---
UID: NN:mpeg2psiparser.IGenericDescriptor
title: IGenericDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\igenericdescriptor.htm
old-project: mstv
ms.assetid: efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IGenericDescriptor, IGenericDescriptor interface [Microsoft TV Technologies], IGenericDescriptor interface [Microsoft TV Technologies],described, IGenericDescriptorInterface, mpeg2psiparser/IGenericDescriptor, mstv.igenericdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mpeg2psiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	IGenericDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IGenericDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IGenericDescriptor</b> enables the client to get an MPEG-2 descriptor in an unparsed format.

See ISO/IEC 1318-1 for the MPEG-2 descriptor specifications. See ETSI EN 300 468 for the DVB descriptor specifications.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGenericDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGenericDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGenericDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbb17e16-b0a4-45c1-b723-cbb6a61d4d0f">GetBody</a>
</td>
<td align="left" width="63%">
Returns the body of the descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd36bb87-ef30-4064-a251-c89a878eeae9">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8923e91-46e1-48fa-a24c-d43cc4a09bd2">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

