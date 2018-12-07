---
UID: NE:mediaobj._DMO_SET_TYPE_FLAGS
title: "_DMO_SET_TYPE_FLAGS"
author: windows-sdk-content
description: The DMO_SET_TYPE_FLAGS enumeration defines flags for setting the media type on a stream.
old-location: dshow\dmo_set_type_flags.htm
tech.root: DirectShow
ms.assetid: e0638668-bbd2-4696-8482-d72438510740
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DMO_SET_TYPEF_CLEAR, DMO_SET_TYPEF_TEST_ONLY, DMO_SET_TYPE_FLAGS , DMO_SET_TYPE_FLAGSEnumeration, _DMO_SET_TYPE_FLAGS, _DMO_SET_TYPE_FLAGS enumeration [DirectShow], dshow.dmo_set_type_flags, mediaobj/DMO_SET_TYPEF_CLEAR, mediaobj/DMO_SET_TYPEF_TEST_ONLY, mediaobj/_DMO_SET_TYPE_FLAGS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mediaobj.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_SET_TYPE_FLAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _DMO_SET_TYPE_FLAGS enumeration


## -description



The <code>DMO_SET_TYPE_FLAGS</code> enumeration defines flags for setting the media type on a stream.




## -enum-fields




### -field DMO_SET_TYPEF_TEST_ONLY

Test the media type but do not set it.


### -field DMO_SET_TYPEF_CLEAR

Clear the media type that was set for the stream.


## -remarks



The DMO_SET_TYPEF_TEST_ONLY and DMO_SET_TYPEF_CLEAR flags are mutually exclusive. Do not set both flags.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/6b466fe4-97a0-46f9-9e4b-461ee66095f1">IMediaObject::SetInputType</a>



<a href="https://msdn.microsoft.com/1dda3c55-d37b-4e04-9509-0e5197d6b019">IMediaObject::SetOutputType</a>
 

 

