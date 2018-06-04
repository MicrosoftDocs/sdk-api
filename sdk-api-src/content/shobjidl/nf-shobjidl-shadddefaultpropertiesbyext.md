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

# SHAddDefaultPropertiesByExt function


## -description


Adds default properties to the property store as registered for the specified file extension.


## -parameters




### -param pszExt [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string that specifies the extension.


### -param pPropStore [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> interface that defines the default properties to add.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The list of properties used to set a default value comes from the <code>SetDefaultsFor</code> registry value of the ProgID for the file association of the specified file extension. The list is prefixed by "<code>prop:</code>" and contains the canonical names of the properties to set the default value, such as: "<code>prop:System.Author;System.Document.DateCreated</code>". The possible properties for this list are <b>System.Author</b>, <b>System.Document.DateCreated</b>, and <b>System.Photo.DateTaken</b>. If the <code>SetDefaultsFor</code> value does not exist on the ProgID, this function uses the default found on the <code>SetDefaultsFor</code> value of <b>HKEY_CLASSES_ROOT\*</b>.

<b>System.Author</b> has the value of the user that performed the action. <b>System.Document.DateCreated</b> and <b>System.Photo.DateTaken</b> use the current date. These three properties are the only ones for which the system provides special defaults.

Note that there are several types of properties: 

                

<ol>
<li>Properties that derive from the file system (such as, size and date created)</li>
<li>Properties that derive from the file (such as, dimensions and number of pages)</li>
<li>Properties that are placed in the file (such as, author and tags)</li>
</ol>
When creating a new file, types one and two are provided just by creating the file. But properties of type three must be set explicitly by a program. The system provides <b>SHAddDefaultPropertiesByExt</b> to provide values for up to three specific properties of type three. Sometimes Windows Explorer uses this API when saving a file for the first time, or when creating a new file after the menu choice <b>New</b> is selected from a shortcut menu.



