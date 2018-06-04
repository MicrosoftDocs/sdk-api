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

# ICategorizer::GetCategoryInfo


## -description


Gets information about a category, such as the default display and the text to display in the UI.


## -parameters




### -param dwCategoryId [in]

Type: <b>DWORD</b>

A <b>DWORD</b> that specifies a category identifier.


### -param pci [out]

Type: <b><a href="https://msdn.microsoft.com/6198cd31-94db-4d31-9cc9-f8b90e661809">CATEGORY_INFO</a>*</b>

When this method returns, contains a pointer to a <a href="https://msdn.microsoft.com/6198cd31-94db-4d31-9cc9-f8b90e661809">CATEGORY_INFO</a> structure that contains the category information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



