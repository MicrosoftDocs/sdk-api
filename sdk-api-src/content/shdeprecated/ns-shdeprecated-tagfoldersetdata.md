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

# tagFolderSetData structure


## -description


<p class="CCE_Message">[<b>FOLDERSETDATA</b> may be altered or unavailable in subsequent versions of the operating system or product.]

Deprecated. Data used in <a href="https://msdn.microsoft.com/fac9323b-bf32-45d0-95c4-798a1aab4d02">IBrowserService2::GetFolderSetData</a>.


## -struct-fields




### -field _fs

Type: <b><a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a></b>

The <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure containing folder view informtion.


### -field _vidRestore

Type: <b>SHELLVIEWID</b>

The last view used for this folder, used as a suggestion for this visit.


### -field _dwViewPriority

Type: <b>DWORD</b>

One of the following values indicating the priority used in choosing the view, listed from highest priority to lowest.



#### VIEW_PRIORITY_RESTRICTED

A Shell restriction is in place that forces this view to be used.



#### VIEW_PRIORITY_CACHEHIT

Current information for this view stored in the registry should be used.



#### VIEW_PRIORITY_STALECACHEHIT

Stored registry information for this view is out of date, so the default view for folders of this type should be used.



#### VIEW_PRIORITY_USEASDEFAULT

The default view for folders of this type should be used.



#### VIEW_PRIORITY_SHELLEXT

The Shell extension determines which view should be used.



#### VIEW_PRIORITY_CACHEMISS

No information on the view is stored in the registry, so the default view for folders of this type should be used.



#### VIEW_PRIORITY_INHERIT

The view from the previous window should be inherited.



#### VIEW_PRIORITY_SHELLEXT_ASBACKUP

If the classic view is operative, the inherited view should be used.



#### VIEW_PRIORITY_DESPERATE

The last known good view supported by the window should be used.



#### VIEW_PRIORITY_NONE

No view is available at this point.

