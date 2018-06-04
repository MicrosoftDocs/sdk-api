---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# REGPINTYPES structure


## -description



The <code>REGPINTYPES</code> structure contains media type information for registering a filter.




## -struct-fields




### -field clsMajorType

Major type GUID of the media type.


### -field clsMinorType

Sub type GUID of the media type. Can be MEDIASUBTYPE_NULL.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> interface to identify the media types that a pin supports. The equivalent <b>AMOVIESETUP_MEDIATYPE</b> type is used in class factory templates (<a href="https://msdn.microsoft.com/3dbe6402-15f8-4490-9fe2-bebaa4e79170">CFactoryTemplate</a>).

To register a range of subtypes within the same major type, use the value MEDIASUBTYPE_NULL.

For more information, see <a href="https://msdn.microsoft.com/2b6304c0-4b67-4723-94a0-7b1fff534f91">How to Register DirectShow Filters</a>.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/c8efe9e6-7d1d-4ec2-ab1b-70ee0798a6a3">Media Types</a>
 

 

