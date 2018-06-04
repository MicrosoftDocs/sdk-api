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

# SHFindFiles function


## -description


<p class="CCE_Message">[<b>SHFindFiles</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays the <b>Search</b> window UI.


## -parameters




### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

The folder from which to start the search. This folder appears in the <b>Look in:</b> box in the <b>Search</b> window. This folder and all of its subfolders are searched unless users choose other options in the <b>Search</b> window's <b>More Advanced Options</b>. This value can be <b>NULL</b>.


### -param pidlSaveFile [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

This parameter is not used and must be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>A saved search file (.fnd) to load. You can save search parameters to a .fnd file after the search is begun. This value can be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful in displaying the <b>Search</b> window; otherwise <b>FALSE</b>.



