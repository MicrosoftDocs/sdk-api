---
UID: NF:xpsobjectmodel.IXpsOMPageReference.SetPrintTicketResource
title: IXpsOMPageReference::SetPrintTicketResource
author: windows-sdk-content
description: Sets the IXpsOMPrintTicketResource interface pointer of the page-level print ticket resource that is to be assigned to the page.
old-location: xps\ixpsompagereference_setprintticketresource.htm
old-project: printdocs
ms.assetid: 76594c7d-327d-45a5-8947-c587ada7b758
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMPageReference interface [XPS Documents and Packaging],SetPrintTicketResource method, IXpsOMPageReference.SetPrintTicketResource, IXpsOMPageReference::SetPrintTicketResource, SetPrintTicketResource, SetPrintTicketResource method [XPS Documents and Packaging], SetPrintTicketResource method [XPS Documents and Packaging],IXpsOMPageReference interface, xps.ixpsompagereference_setprintticketresource, xpsobjectmodel/IXpsOMPageReference::SetPrintTicketResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IXpsOMPageReference.SetPrintTicketResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPageReference::SetPrintTicketResource


## -description


Sets  the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface pointer of the page-level print ticket resource that is to be assigned to the page.


## -parameters




### -param printTicketResource [in]

A pointer to the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of the page-level print ticket resource that is to be assigned to the page. If a print ticket has already been set, a <b>NULL</b> pointer releases it.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>printTicketResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

