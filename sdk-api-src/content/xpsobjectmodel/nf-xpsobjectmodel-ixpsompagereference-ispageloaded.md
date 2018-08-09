---
UID: NF:xpsobjectmodel.IXpsOMPageReference.IsPageLoaded
title: IXpsOMPageReference::IsPageLoaded
author: windows-sdk-content
description: Gets the referenced page status, which indicates whether the page is loaded.
old-location: xps\ixpsompagereference_ispageloaded.htm
old-project: printdocs
ms.assetid: 12b7d824-65eb-4d24-bfb6-40f55085186c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FALSE, IXpsOMPageReference interface [XPS Documents and Packaging],IsPageLoaded method, IXpsOMPageReference.IsPageLoaded, IXpsOMPageReference::IsPageLoaded, IsPageLoaded, IsPageLoaded method [XPS Documents and Packaging], IsPageLoaded method [XPS Documents and Packaging],IXpsOMPageReference interface, TRUE, xps.ixpsompagereference_ispageloaded, xpsobjectmodel/IXpsOMPageReference::IsPageLoaded
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
 - IXpsOMPageReference.IsPageLoaded
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPageReference::IsPageLoaded


## -description


Gets the referenced page status,  which indicates whether the  page is loaded.


## -parameters




### -param isPageLoaded [out, retval]

A Boolean value that indicates the status of the page.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The page is loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The page is not loaded.

</td>
</tr>
</table>
 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>isPageLoaded</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>
 

 

