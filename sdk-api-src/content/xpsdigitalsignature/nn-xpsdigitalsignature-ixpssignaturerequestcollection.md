---
UID: NN:xpsdigitalsignature.IXpsSignatureRequestCollection
title: IXpsSignatureRequestCollection
author: windows-driver-content
description: A collection of IXpsSignatureRequest interfaces.
old-location: xps\ixpssignaturerequestcollection.htm
old-project: printdocs
ms.assetid: bb8279e1-a98b-4156-8b90-d9b69411bfa3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsSignatureRequestCollection, IXpsSignatureRequestCollection interface [XPS Documents and Packaging], IXpsSignatureRequestCollection interface [XPS Documents and Packaging],described, xps.ixpssignaturerequestcollection, xpsdigitalsignature/IXpsSignatureRequestCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsdigitalsignature.h
api_name:
-	IXpsSignatureRequestCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureRequestCollection interface


## -description


A collection of <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsSignatureRequestCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsSignatureRequestCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsSignatureRequestCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">

              Gets an <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">

              Gets the number of <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointers in the collection.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597596">RemoveAt</a>
</td>
<td align="left" width="63%">

              Removes and releases an <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer from a specified location in the collection.
            

</td>
</tr>
</table> 


## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

