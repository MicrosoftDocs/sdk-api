---
UID: NE:shlwapi.ASSOCDATA
title: ASSOCDATA
author: windows-sdk-content
description: Used by IQueryAssociations::GetData to define the type of data that is to be returned.
old-location: shell\ASSOCDATA_str.htm
tech.root: shell
ms.assetid: 0ae5c8db-81fd-4d00-8e54-0c474f1bfd06
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: ASSOCDATA, ASSOCDATA enumeration [Windows Shell], ASSOCDATA_EDITFLAGS, ASSOCDATA_HASPERUSERASSOC, ASSOCDATA_MSIDESCRIPTOR, ASSOCDATA_NOACTIVATEHANDLER, ASSOCDATA_QUERYCLASSSTORE, ASSOCDATA_VALUE, _win32_ASSOCDATA_str, shell.ASSOCDATA_str, shlwapi/ASSOCDATA, shlwapi/ASSOCDATA_EDITFLAGS, shlwapi/ASSOCDATA_HASPERUSERASSOC, shlwapi/ASSOCDATA_MSIDESCRIPTOR, shlwapi/ASSOCDATA_NOACTIVATEHANDLER, shlwapi/ASSOCDATA_QUERYCLASSSTORE, shlwapi/ASSOCDATA_VALUE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - ASSOCDATA
product: Windows
targetos: Windows
req.typenames: ASSOCDATA
req.redist: 
---

# ASSOCDATA enumeration


## -description


Used by <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> to define the type of data that is to be returned.


## -enum-fields




### -field ASSOCDATA_MSIDESCRIPTOR

The component descriptor to pass to the Windows Installer API.


### -field ASSOCDATA_NOACTIVATEHANDLER

Attempts to activate a window are restricted. There is no data associated with this value.


### -field ASSOCDATA_UNUSED1


### -field ASSOCDATA_HASPERUSERASSOC

Defaults to user specified association.


### -field ASSOCDATA_EDITFLAGS

<b>Internet Explorer version 6 or later</b>. Gets the data stored in the EditFlags value of a file association <a href="https://msdn.microsoft.com/f2b666d6-bf22-47b5-87e1-8de5ff51c152">PROGID</a> registry key. This value consists of one or more <a href="https://msdn.microsoft.com/63b58659-9c4c-4b39-98d1-743724523dcd">FILETYPEATTRIBUTEFLAGS</a>. Compare against those values to determine which attributes have been set.


### -field ASSOCDATA_VALUE

<b>Internet Explorer version 6 or later</b>. Uses the <i>pwszExtra</i> parameter from the <a href="https://msdn.microsoft.com/7f21e564-97c6-4f9d-a4fa-160b78dbfc2f">IQueryAssociations::GetData</a> method as the value name.


### -field ASSOCDATA_MAX




#### - ASSOCDATA_QUERYCLASSSTORE

If this value is present, applications should check the Windows 2000 class store.

