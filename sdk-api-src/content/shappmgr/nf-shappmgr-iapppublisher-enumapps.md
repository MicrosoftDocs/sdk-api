---
UID: NF:shappmgr.IAppPublisher.EnumApps
title: IAppPublisher::EnumApps
author: windows-sdk-content
description: Creates an enumerator for enumerating all applications published by an application publisher for a given category.
old-location: shell\IAppPublisher_EnumApps.htm
tech.root: shell
ms.assetid: b24c3007-662a-4c42-9ca7-367180152deb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumApps, EnumApps method [Windows Shell], EnumApps method [Windows Shell],IAppPublisher interface, IAppPublisher interface [Windows Shell],EnumApps method, IAppPublisher.EnumApps, IAppPublisher::EnumApps, inet_IAppPublisher_EnumApps, shappmgr/IAppPublisher::EnumApps, shell.IAppPublisher_EnumApps
ms.topic: method
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - Shappmgr.h
api_name:
 - IAppPublisher.EnumApps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppPublisher::EnumApps


## -description


Creates an enumerator for enumerating all applications published by an application publisher for a given category.


## -parameters




### -param pAppCategoryId [in]

Type: <b>GUID*</b>

A pointer to a GUID that specifies the application category to be enumerated. This must be one of the categories provided through <a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>. If <i>pAppCategoryID</i> identifies a category not provided through <b>IAppPublisher::GetCategories</b>, creation of the enumerator succeeds with the enumerator returning zero items. If this parameter value is <b>NULL</b>, the enumerator returns applications published for all categories.


### -param ppepa [out]

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
 

 

