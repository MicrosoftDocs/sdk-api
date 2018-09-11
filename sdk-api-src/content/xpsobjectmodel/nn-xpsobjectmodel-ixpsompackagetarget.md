---
UID: NN:xpsobjectmodel.IXpsOMPackageTarget
title: IXpsOMPackageTarget
author: windows-sdk-content
description: Provides the method to create an IXpsOMPackageWriter that can be used by a print job that was created by the StartXpsPrintJob1 function.
old-location: xps\ixpsompackagetarget.htm
tech.root: printdocs
ms.assetid: 980D2A37-933F-41B1-A975-6BC797E8E770
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMPackageTarget, IXpsOMPackageTarget interface [XPS Documents and Packaging], IXpsOMPackageTarget interface [XPS Documents and Packaging],described, xps.ixpsompackagetarget, xpsobjectmodel/IXpsOMPackageTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 with SP1, Windows Server 2008 and Platform Update Supplement for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: XpsPrint.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XpsPrint.lib
 - XpsPrint.dll
api_name:
 - IXpsOMPackageTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackageTarget interface


## -description


Provides the method to create an <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> that can be used by a print job that was created by the  <a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackageTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPackageTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackageTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6AD4BEB8-86B7-4085-9B84-D723982933FE">CreateXpsOMPackageWriter</a>
</td>
<td align="left" width="63%">
Create an <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface for use with a print job that the  <a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a> function created.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface writes the application data in the order in which they will appear to the user.

To create an instance of an <b>IXpsOMPackageTarget</b> interface, call the <a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a> function.

To create the <a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a> interface to use to write the document to a printer, call the <a href="https://msdn.microsoft.com/6AD4BEB8-86B7-4085-9B84-D723982933FE">CreateXpsOMPackageWriter</a> method of this interface.




## -see-also




<a href="https://msdn.microsoft.com/cbbcc8bf-6172-41c8-9d74-27e5635ec167">IXpsOMPackageWriter</a>



<a href="https://msdn.microsoft.com/91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D">StartXpsPrintJob1</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

