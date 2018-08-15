---
UID: NE:cscobj.tagOFFLINEFILES_PATHFILTER_MATCH
title: tagOFFLINEFILES_PATHFILTER_MATCH
author: windows-sdk-content
description: Specifies how closely an event must match a filter.
old-location: of\offlinefiles_pathfilter_match.htm
old-project: offlinefiles
ms.assetid: fae3d36d-b5f3-45ae-97f2-41fd6045d976
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OFFLINEFILES_PATHFILTER_CHILD, OFFLINEFILES_PATHFILTER_DESCENDENT, OFFLINEFILES_PATHFILTER_MATCH, OFFLINEFILES_PATHFILTER_MATCH enumeration [Offline Files], OFFLINEFILES_PATHFILTER_SELF, OFFLINEFILES_PATHFILTER_SELFORCHILD, OFFLINEFILES_PATHFILTER_SELFORDESCENDENT, cscobj/OFFLINEFILES_PATHFILTER_CHILD, cscobj/OFFLINEFILES_PATHFILTER_DESCENDENT, cscobj/OFFLINEFILES_PATHFILTER_MATCH, cscobj/OFFLINEFILES_PATHFILTER_SELF, cscobj/OFFLINEFILES_PATHFILTER_SELFORCHILD, cscobj/OFFLINEFILES_PATHFILTER_SELFORDESCENDENT, of.offlinefiles_pathfilter_match, tagOFFLINEFILES_PATHFILTER_MATCH
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: cscobj.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFFLINEFILES_PATHFILTER_MATCH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_PATHFILTER_MATCH
product: Windows
targetos: Windows
req.lib: CscApi.lib
req.dll: CscApi.dll
req.irql: 
---

# tagOFFLINEFILES_PATHFILTER_MATCH enumeration


## -description


Specifies how closely an event must match a filter.


## -enum-fields




### -field OFFLINEFILES_PATHFILTER_SELF

Event must be an exact match for the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_CHILD

Event must be for an immediate child of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_DESCENDENT

Event can be any descendant of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_SELFORCHILD

Event must be an exact match or an immediate child of the fully qualified UNC path associated with the filter.


### -field OFFLINEFILES_PATHFILTER_SELFORDESCENDENT

Event must be an exact match or any descendant of the fully qualified UNC path associated with the filter.


## -see-also




<a href="https://msdn.microsoft.com/0b9d8339-3daa-4f0c-8a52-59e06b663163">IOfflineFilesEventsFilter::GetPathFilter</a>
 

 

