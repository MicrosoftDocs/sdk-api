---
UID: NN:xpsobjectmodel_1.IXpsOMPage1
title: IXpsOMPage1
author: windows-sdk-content
description: Inherits from IXpsOMPage.
old-location: xps\ixpsompage1.htm
tech.root: printdocs
ms.assetid: 4f4ec7d9-da77-4d34-89aa-a73250c0e610
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMPage1, IXpsOMPage1 interface [XPS Documents and Packaging], IXpsOMPage1 interface [XPS Documents and Packaging],described, xps.ixpsompage1, xpsobjectmodel_1/IXpsOMPage1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: xpsobjectmodel_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: None
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - none
 - none.dll
api_name:
 - IXpsOMPage1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPage1 interface


## -description


Inherits from IXpsOMPage. 

Provides support for:

Detecting the type of XPS FixedPage markup which this page was loaded from.

Serializing page objects to markup of the requested type - MSXPS or OpenXps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPage1</b> interface inherits from <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>. <b>IXpsOMPage1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPage1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2456ffc-7a9d-41c2-b693-eb71909ccf3d">IXpsOMPage1::GetDocumentType</a>
</td>
<td align="left" width="63%">
Gets the type of FixedPage markup that was used to initialize this page. This method is used to determine whether a document is the XPS or OpenXPS type. For more information, see <a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">XPS Documents</a>.

</td>
</tr>
</table> 


## -remarks



<h3><a id="Additional_References"></a><a id="additional_references"></a><a id="ADDITIONAL_REFERENCES"></a>Additional References</h3>
The base interface is defined and documented in Windows 7 SDK.

http://msdn.microsoft.com/en-us/library/dd372635(v=VS.85).aspx




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>
 

 

