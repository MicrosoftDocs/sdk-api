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

# _tagITEMPROP structure


## -description


<p class="CCE_Message">[<b>ITEMPROP</b> and <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> are supported only on Windows XP and Windows Server 2003, and should no longer be used.]

Stores information about properties in the <a href="https://msdn.microsoft.com/c2094bbe-a4ca-4f30-b16e-14dced2912bc">Windows Property System</a>, and is used by the <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> interface.


## -struct-fields




### -field variantValue

 


### -field pwszName

 




#### - bstrIndexProp

The name of a property in the <a href="https://msdn.microsoft.com/c2094bbe-a4ca-4f30-b16e-14dced2912bc">Windows Property System</a>. For example, the <a href="https://msdn.microsoft.com/d592f12b-f8c2-406f-a031-eeb8212e64f7">System.ItemUrl</a> property.


#### - bstrName

For internal use only.


#### - ds

For internal use only.


#### - dwHint

For internal use only.


#### - dwUID

For internal use only.


#### - vt

The type of the property value. For example, the type of the string property <a href="https://msdn.microsoft.com/d592f12b-f8c2-406f-a031-eeb8212e64f7">System.ItemUrl</a> is <b>VT_BSTR</b>. 


## -remarks



To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the <a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a> interface and the following APIs: the <a href="https://msdn.microsoft.com/b52fd64b-b03a-4d02-a64f-201f6b7d5045">ISearchProtocolUI</a>, <a href="https://msdn.microsoft.com/d7d6cbb0-18bf-4e68-b7b4-307cadbced5c">IItemPreviewerExt</a> and <a href="https://msdn.microsoft.com/e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd">ISearchItem</a> interfaces, the <a href="https://msdn.microsoft.com/c1d525ea-ee80-49fb-9447-20465b8f8654">LINKINFO</a> and <b>ITEMPROP</b> structures, and the <a href="https://msdn.microsoft.com/2a0ddb31-df35-4da5-9950-b091cd461556">LINKTYPE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0fef34c5-f20f-475a-9223-5cb73079c842">IItemPropertyBag</a>
 

 

