---
UID: NF:dmoimpl.IMediaObjectImpl.OutputType
title: IMediaObjectImpl::OutputType (dmoimpl.h)
author: windows-sdk-content
description: The OutputType method retrieves the current media type for a specified output stream.
old-location: dshow\imediaobjectimpl_outputtype.htm
tech.root: DirectShow
ms.assetid: 46831756-ed3b-40de-80ad-21874db283c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaObjectImpl interface [DirectShow],OutputType method, IMediaObjectImpl.OutputType, IMediaObjectImpl::OutputType, IMediaObjectImplOutputType, OutputType, OutputType method [DirectShow], OutputType method [DirectShow],IMediaObjectImpl interface, dmoimpl/IMediaObjectImpl::OutputType, dshow.imediaobjectimpl_outputtype
ms.topic: method
req.header: dmoimpl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib; Msdmo.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
 - Msdmo.lib
 - Msdmo.dll
api_name:
 - IMediaObjectImpl.OutputType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaObjectImpl::OutputType


## -description



The <code>OutputType</code> method retrieves the current media type for a specified output stream.




## -parameters




### -param ulOutputStreamIndex

Index of an output stream.


## -returns



Returns a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd375504(v=VS.85).aspx">DMO_MEDIA_TYPE</a> structure, or <b>NULL</b> if the type is not set for this stream.




## -see-also




<a href="https://msdn.microsoft.com/81d45b8d-8373-4e42-b768-f6126feb935d">IMediaObjectImpl Class Template</a>
 

 

