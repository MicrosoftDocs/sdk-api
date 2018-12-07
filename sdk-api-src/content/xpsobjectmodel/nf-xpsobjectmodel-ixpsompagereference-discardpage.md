---
UID: NF:xpsobjectmodel.IXpsOMPageReference.DiscardPage
title: IXpsOMPageReference::DiscardPage
author: windows-sdk-content
description: Discards the page from memory.
old-location: xps\ixpsompagereference_discardpage.htm
tech.root: printdocs
ms.assetid: 430b9169-7fc5-493d-85a8-dddf46dfef8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscardPage, DiscardPage method [XPS Documents and Packaging], DiscardPage method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],DiscardPage method, IXpsOMPageReference.DiscardPage, IXpsOMPageReference::DiscardPage, xps.ixpsompagereference_discardpage, xpsobjectmodel/IXpsOMPageReference::DiscardPage
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPageReference.DiscardPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPageReference::DiscardPage


## -description


Discards the page from memory.


## -parameters






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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/430b9169-7fc5-493d-85a8-dddf46dfef8f">DiscardPage</a> has been called more than once or the page has not been loaded.

</td>
</tr>
</table>
 




## -remarks



If <a href="https://msdn.microsoft.com/7d1381ad-6ac8-4ea4-99a2-8bc5d95773c7">SetPage</a> has not been called, calling <b>DiscardPage</b> and then <a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">GetPage</a> will return the virtualized page from the source package. If <b>SetPage</b> has been called, calling <b>DiscardPage</b> and then  <b>GetPage</b> will return <b>NULL</b>.
        

If the page referenced by this <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface has been constructed entirely in memory and does not have a corresponding file, <b>DiscardPage</b> will delete the page from memory and the page's content will be lost. If the page has been constructed from a file, <b>DiscardPage</b> will delete the page from memory but will not alter the original file. The page can be reconstructed and read back into memory by calling <a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">GetPage</a>.

If the page has been constructed from a file and subsequently modified, <b>DiscardPage</b> will discard the page from memory, and any changes made to the page will be lost. Calling <a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">GetPage</a> after this will re-read the original content from the file.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">IXpsOMPageReference::GetPage</a>



<a href="https://msdn.microsoft.com/7d1381ad-6ac8-4ea4-99a2-8bc5d95773c7">IXpsOMPageReference::SetPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

