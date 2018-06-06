---
UID: NF:xpsobjectmodel.IXpsOMImageResource.SetContent
title: IXpsOMImageResource::SetContent
author: windows-sdk-content
description: Sets the read-only stream to be associated with this resource.
old-location: xps\ixpsomimageresource_setcontent.htm
old-project: printdocs
ms.assetid: 91dc565f-4ccb-497c-b5d2-f9b60884b094
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMImageResource interface [XPS Documents and Packaging],SetContent method, IXpsOMImageResource.SetContent, IXpsOMImageResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMImageResource interface, xps.ixpsomimageresource_setcontent, xpsobjectmodel/IXpsOMImageResource::SetContent
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMImageResource.SetContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageResource::SetContent


## -description


Sets the read-only stream to be associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param imageType [in]

The  <a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a> value that describes the type of image in the stream.


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

Because <a href="https://msdn.microsoft.com/30d90686-67f5-4e18-811b-472e6a00538f">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/b4300a8c-f0bf-465f-a717-c54de95c1183">XPS_IMAGE_TYPE</a>
 

 

