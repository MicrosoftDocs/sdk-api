---
UID: NN:objidl.IAgileReference
title: IAgileReference (objidl.h)

description: Enables retrieving an agile reference to an object.
old-location: winrt\iagilereference.htm
tech.root: WinRT
ms.assetid: 51787A45-BCDE-4028-A338-1C16F2DE79AD

ms.date: 12/05/2018
ms.keywords: IAgileReference, IAgileReference interface [Windows Runtime], IAgileReference interface [Windows Runtime],described, objidl/IAgileReference, winrt.iagilereference
ms.topic: interface
f1_keywords: 
 - "objidl/IAgileReference"
dev_langs:
 - c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IAgileReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAgileReference interface


## -description


Enables retrieving an agile reference to an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAgileReference</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAgileReference</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/WinRT/iagilereference-resolve">Resolve</a>
</td>
<td align="left" width="63%">
Gets the interface ID of an agile reference to an object.

</td>
</tr>
</table> 


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-rogetagilereference">RoGetAgileReference</a> function to create an agile reference to an object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-rogetagilereference">RoGetAgileReference</a>
 

 

