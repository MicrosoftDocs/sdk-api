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

# ICategoryProvider::CanCategorizeOnSCID


## -description


Determines whether a column can be used as a category.


## -parameters




### -param pscid [in]

Type: <b>const <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/bf7b0e3b-527a-4ef5-894a-a7e1b7750e72">SHCOLUMNID</a> structure that identifies the column. Valid only when S_OK is returned. The GUID contained in this structure is then passed to <a href="https://msdn.microsoft.com/3703c061-4d21-4c36-900a-9ccacf4d482a">ICategoryProvider::CreateCategory</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the column can be used as a category or S_FALSE if not.




## -remarks



When using the System Folder View Object in Category view (<b>Show in Groups</b>), the titles of columns for which this method returns S_OK appear in the upper portion of the <b>Arrange Icons By</b> submenu.



