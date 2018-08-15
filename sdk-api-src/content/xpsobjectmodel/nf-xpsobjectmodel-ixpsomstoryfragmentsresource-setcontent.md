---
UID: NF:xpsobjectmodel.IXpsOMStoryFragmentsResource.SetContent
title: IXpsOMStoryFragmentsResource::SetContent
author: windows-sdk-content
description: Sets the read-only stream to be associated with this resource.
old-location: xps\ixpsomstoryfragmentsresource_setcontent.htm
old-project: printdocs
ms.assetid: 861d9688-932b-4830-b52b-acd505524608
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],SetContent method, IXpsOMStoryFragmentsResource.SetContent, IXpsOMStoryFragmentsResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMStoryFragmentsResource interface, xps.ixpsomstoryfragmentsresource_setcontent, xpsobjectmodel/IXpsOMStoryFragmentsResource::SetContent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
 - IXpsOMStoryFragmentsResource.SetContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMStoryFragmentsResource::SetContent


## -description


Sets the read-only stream to be associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

For more information about the content of a StoryFragments part, see the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.

Because <a href="https://msdn.microsoft.com/c119f1c6-59c0-41b2-b79d-5de9a62c146a">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

