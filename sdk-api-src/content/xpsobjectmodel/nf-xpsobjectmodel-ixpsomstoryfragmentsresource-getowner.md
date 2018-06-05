---
UID: NF:xpsobjectmodel.IXpsOMStoryFragmentsResource.GetOwner
title: IXpsOMStoryFragmentsResource::GetOwner
author: windows-sdk-content
description: Gets a pointer to the IXpsOMPage interface that contains this resource.
old-location: xps\ixpsomstoryfragmentsresource_getowner.htm
old-project: printdocs
ms.assetid: 8dc44277-d296-4747-8dd7-8901a94b5213
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMStoryFragmentsResource interface, IXpsOMStoryFragmentsResource interface [XPS Documents and Packaging],GetOwner method, IXpsOMStoryFragmentsResource.GetOwner, IXpsOMStoryFragmentsResource::GetOwner, xps.ixpsomstoryfragmentsresource_getowner, xpsobjectmodel/IXpsOMStoryFragmentsResource::GetOwner
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMStoryFragmentsResource.GetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMStoryFragmentsResource::GetOwner


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains this resource.


## -parameters




### -param owner [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains this resource. If the resource is not part of a page, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/83bc8017-c679-40a8-96a8-bff9aa2273af">IXpsOMStoryFragmentsResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

