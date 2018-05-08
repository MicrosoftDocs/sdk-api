---
UID: NN:xpsobjectmodel.IXpsOMDashCollection
title: IXpsOMDashCollection
author: windows-driver-content
description: A collection of XPS_DASH structures.
old-location: xps\ixpsomdashcollection.htm
old-project: printdocs
ms.assetid: 02a152a1-e117-42fb-8428-a2b28e6540a9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDashCollection, IXpsOMDashCollection interface [XPS Documents and Packaging], IXpsOMDashCollection interface [XPS Documents and Packaging],described, xps.ixpsomdashcollection, xpsobjectmodel/IXpsOMDashCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMDashCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDashCollection interface


## -description


A collection of <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMDashCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMDashCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMDashCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8d2baf5-e36e-4363-bde6-1731c97e702f">Append</a>
</td>
<td align="left" width="63%">

              Appends an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure to the end of the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">

              Gets an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">

              Gets the number of <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structures in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9ef0ea9-f427-41ff-b33e-c9b5f49cb7d9">InsertAt</a>
</td>
<td align="left" width="63%">

              Inserts an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure at a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597596">RemoveAt</a>
</td>
<td align="left" width="63%">

              Removes and frees an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0ea0ae0-2c28-4478-82fc-3e80bc70eef8">SetAt</a>
</td>
<td align="left" width="63%">

              Replaces an <a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a> structure at a specified location in the collection.
            

</td>
</tr>
</table> 


## -remarks



For more information about the collection methods, see <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/c8f43f91-eefb-4025-8042-c2601e89d315">XPS_DASH</a>
 

 

