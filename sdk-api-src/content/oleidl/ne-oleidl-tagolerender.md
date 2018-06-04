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

# tagOLERENDER enumeration


## -description


Indicates the type of caching requested for newly created objects.


## -enum-fields




### -field OLERENDER_NONE

The client is not requesting any locally cached drawing or data retrieval capabilities in the object. The <i>pFormatEtc</i> parameter of the calls is ignored when this value is specified for the <i>renderopts</i> parameter.


### -field OLERENDER_DRAW

The client will draw the content of the object on the screen (a <b>NULL</b> target device) using <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>. The object itself determines the data formats that need to be cached. With this render option, only the <b>ptd</b> and <b>dwAspect</b> members of <i>pFormatEtc</i> are significant, since the object may cache things differently depending on the parameter values. However, <i>pFormatEtc</i> can legally be <b>NULL</b> here, in which case the object is to assume the display target device and the DVASPECT_CONTENT aspect.


### -field OLERENDER_FORMAT

The client will pull one format from the object using <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. The format of the data to be cached is passed in <i>pFormatEtc</i>, which may not in this case be <b>NULL</b>.


### -field OLERENDER_ASIS

The client is not requesting any locally cached drawing or data retrieval capabilities in the object. <i>pFormatEtc</i> is ignored for this option. The difference between this and the OLERENDER_FORMAT value is important in such functions as <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> and <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a>. 



## -see-also




<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>



<a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a>



<a href="https://msdn.microsoft.com/98c63646-6617-46b6-8c3e-82d1c4d0adb6">OleCreateFromFile</a>



<a href="https://msdn.microsoft.com/ef52dc37-aa63-47f3-a04f-f9d22178690f">OleCreateLink</a>



<a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a>



<a href="https://msdn.microsoft.com/06b013db-0554-4dbc-b19d-28314fb4fee0">OleCreateLinkToFile</a>



<a href="https://msdn.microsoft.com/847d82f5-149d-48a4-a228-f5551a07a790">OleCreateStaticFromData</a>
 

 

