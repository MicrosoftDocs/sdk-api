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

# _SFVM_PROPPAGE_DATA structure


## -description


Contains the details of a page to be added to an object's <b>Properties</b> sheet.


## -struct-fields




### -field dwReserved

Type: <b>DWORD</b>


### -field pfn

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to a <a href="https://msdn.microsoft.com/37673813-89dc-4624-a58b-fe5f44df46c6">AddPropSheetPageProc</a> callback function used to add property pages. When this function is used by Windows Explorer, it provides <b>pfn</b> through the system folder view object's <a href="https://msdn.microsoft.com/6f05ddf7-190e-41f5-b24a-d18112b34600">IShellView::AddPropertySheetPages</a> method. The callback function can then pass the information to <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a>.


### -field lParam

Type: <b>LPARAM</b>

The details of the property sheet to be added. When this function is used by Windows Explorer, it provides <b>lParam</b> through the system folder view object's <a href="https://msdn.microsoft.com/6f05ddf7-190e-41f5-b24a-d18112b34600">IShellView::AddPropertySheetPages</a> method. The callback function can then pass the information to <a href="https://msdn.microsoft.com/76a2a94b-b79f-41d1-9e42-fbfda545d12f">IShellPropSheetExt::AddPages</a>.

