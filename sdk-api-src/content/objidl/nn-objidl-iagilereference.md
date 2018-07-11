---
UID: NN:objidl.IAgileReference
title: IAgileReference
author: windows-sdk-content
description: Enables retrieving an agile reference to an object.
old-location: winrt\iagilereference.htm
old-project: WinRT
ms.assetid: 51787A45-BCDE-4028-A338-1C16F2DE79AD
ms.author: windowssdkdev
ms.date: 07/06/2018
ms.keywords: IAgileReference, IAgileReference interface [Windows Runtime], IAgileReference interface [Windows Runtime],described, objidl/IAgileReference, winrt.iagilereference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IAgileReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAgileReference interface


## -description


Enables retrieving an agile reference to an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAgileReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAgileReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAgileReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/627A7EE4-CFEF-47F6-BA99-51BEB78C5D55">Resolve</a>
</td>
<td align="left" width="63%">
Gets the interface ID of an agile reference to an object.

</td>
</tr>
</table> 


## -remarks



Call the <a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a> function to create an agile reference to an object.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/D16224C7-1BB7-46F5-B66C-54D0B9679006">RoGetAgileReference</a>
 

 

