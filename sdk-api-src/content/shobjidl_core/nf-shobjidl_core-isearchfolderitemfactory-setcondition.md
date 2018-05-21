---
UID: NF:shobjidl_core.ISearchFolderItemFactory.SetCondition
title: ISearchFolderItemFactory::SetCondition
author: windows-driver-content
description: Sets the ICondition of the search. When this method is not called, the resulting search will have no filters applied.
old-location: shell\ISearchFolderItemFactory_SetCondition.htm
old-project: shell
ms.assetid: 6ac5acc3-e522-4b6f-a31c-c0850445e00c
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ISearchFolderItemFactory interface [Windows Shell],SetCondition method, ISearchFolderItemFactory.SetCondition, ISearchFolderItemFactory::SetCondition, SetCondition, SetCondition method [Windows Shell], SetCondition method [Windows Shell],ISearchFolderItemFactory interface, _shell_ISearchFolderItemFactory_SetCondition, shell.ISearchFolderItemFactory_SetCondition, shobjidl_core/ISearchFolderItemFactory::SetCondition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ISearchFolderItemFactory.SetCondition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISearchFolderItemFactory::SetCondition


## -description


Sets the  <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> of the search.  When this method is not called, the resulting search will have no filters applied.


## -parameters




### -param pCondition [in]

Type: <b><a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> interface.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="_search_ICondition_Clone">ICondition::Clone</a>



<a href="https://msdn.microsoft.com/a684b373-6de4-4b4a-bbae-85e1c5a7e04a">ISearchFolderItemFactory</a>
 

 

