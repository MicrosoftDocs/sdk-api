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

# IAppPublisher::EnumApps


## -description


Creates an enumerator for enumerating all applications published by an application publisher for a given category.


## -parameters




### -param pAppCategoryId




### -param ppepa






#### - pAppCategoryID [in]

Type: <b>GUID*</b>

A pointer to a GUID that specifies the application category to be enumerated. This must be one of the categories provided through <a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>. If <i>pAppCategoryID</i> identifies a category not provided through <b>IAppPublisher::GetCategories</b>, creation of the enumerator succeeds with the enumerator returning zero items. If this parameter value is <b>NULL</b>, the enumerator returns applications published for all categories.


#### - ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a> reference variable that points to a <b>IEnumPublishedApps</b> interface. Application publishers must create an enumeration object that supports the <b>IEnumPublishedApps</b> interface, and return its pointer value through this parameter.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a> is not a standard enumeration interface. It does not support a Skip method nor does its Next method support retrieval of multiple items.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>



<a href="https://msdn.microsoft.com/89a06b1d-1b72-46ca-91cd-bb63ea0cbff7">IEnumPublishedApps</a>



<a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>
 

 

