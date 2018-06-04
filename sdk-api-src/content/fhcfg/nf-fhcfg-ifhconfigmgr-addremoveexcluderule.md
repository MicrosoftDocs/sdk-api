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

# IFhConfigMgr::AddRemoveExcludeRule


## -description


Adds an exclusion rule to the exclusion list or removes a  rule from the list.


## -parameters




### -param Add [in]

If this parameter is <b>TRUE</b>, a new exclusion rule is added.
If it is set to <b>FALSE</b>, an existing exclusion rule is removed.


### -param Category [in]

Specifies the type of the exclusion rule. See the <a href="https://msdn.microsoft.com/40AE4FB7-B81D-4CC1-B1A2-53952AE538DD">FH_PROTECTED_ITEM_CATEGORY</a> enumeration for possible values.


### -param Item [in]

The folder path or library name or GUID of the item that the exclusion rule applies to.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



The File History protection scope is the set of files that are backed up by the File History feature.  It contains inclusion rules and exclusion rules. Inclusion rules specify the files and folders that are included. Exclusion rules specify the files and folders that are excluded.

The default protection scope includes all folders from all user libraries and the  Contacts, Desktop, and Favorites folders.

Exclusion rules take precedence over inclusion rules. In other words, if an inclusion rule conflicts with an exclusion rule, the File History feature follows the exclusion rule.

To reduce the protection scope, use the <b>IFhConfigMgr::AddRemoveExcludeRule</b> to add exclusion rules. 

This method can be used to add or remove exclusion rules. It cannot be used to modify inclusion rules.

User libraries can be enumerated by calling the <a href="https://msdn.microsoft.com/d0880a8c-20dd-47cc-b6c5-23dedb32d453">SHGetKnownFolderItem</a> function and the methods of the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> and <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> interfaces.

Standard folders and libraries are specified by a GUID, prefixed with an asterisk. For example,  *a990ae9f-a03b-4e80-94bc-9912d7504104 specifies the Pictures library. For a list of standard folders and libraries and their GUIDs, see the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> documentation. 

Custom libraries are specified by name. Folders are specified by their full path (for example, C:\Users\Public\Videos).




## -see-also




<a href="https://msdn.microsoft.com/40AE4FB7-B81D-4CC1-B1A2-53952AE538DD">FH_PROTECTED_ITEM_CATEGORY</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a>
 

 

