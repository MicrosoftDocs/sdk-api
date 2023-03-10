---
UID: NE:cscobj.tagOFFLINEFILES_PATHFILTER_MATCH
title: OFFLINEFILES_PATHFILTER_MATCH (cscobj.h)
description: Specifies how closely an event must match a filter.
helpviewer_keywords: ["OFFLINEFILES_PATHFILTER_CHILD","OFFLINEFILES_PATHFILTER_DESCENDENT","OFFLINEFILES_PATHFILTER_MATCH","OFFLINEFILES_PATHFILTER_MATCH enumeration [Offline Files]","OFFLINEFILES_PATHFILTER_SELF","OFFLINEFILES_PATHFILTER_SELFORCHILD","OFFLINEFILES_PATHFILTER_SELFORDESCENDENT","cscobj/OFFLINEFILES_PATHFILTER_CHILD","cscobj/OFFLINEFILES_PATHFILTER_DESCENDENT","cscobj/OFFLINEFILES_PATHFILTER_MATCH","cscobj/OFFLINEFILES_PATHFILTER_SELF","cscobj/OFFLINEFILES_PATHFILTER_SELFORCHILD","cscobj/OFFLINEFILES_PATHFILTER_SELFORDESCENDENT","of.offlinefiles_pathfilter_match"]
old-location: of\offlinefiles_pathfilter_match.htm
tech.root: of
ms.assetid: fae3d36d-b5f3-45ae-97f2-41fd6045d976
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_PATHFILTER_CHILD, OFFLINEFILES_PATHFILTER_DESCENDENT, OFFLINEFILES_PATHFILTER_MATCH, OFFLINEFILES_PATHFILTER_MATCH enumeration [Offline Files], OFFLINEFILES_PATHFILTER_SELF, OFFLINEFILES_PATHFILTER_SELFORCHILD, OFFLINEFILES_PATHFILTER_SELFORDESCENDENT, cscobj/OFFLINEFILES_PATHFILTER_CHILD, cscobj/OFFLINEFILES_PATHFILTER_DESCENDENT, cscobj/OFFLINEFILES_PATHFILTER_MATCH, cscobj/OFFLINEFILES_PATHFILTER_SELF, cscobj/OFFLINEFILES_PATHFILTER_SELFORCHILD, cscobj/OFFLINEFILES_PATHFILTER_SELFORDESCENDENT, of.offlinefiles_pathfilter_match
req.header: cscobj.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFFLINEFILES_PATHFILTER_MATCH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_PATHFILTER_MATCH
 - cscobj/tagOFFLINEFILES_PATHFILTER_MATCH
 - OFFLINEFILES_PATHFILTER_MATCH
 - cscobj/OFFLINEFILES_PATHFILTER_MATCH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_PATHFILTER_MATCH
---

# OFFLINEFILES_PATHFILTER_MATCH enumeration


## -description

Specifies how closely an event must match a filter.

## -enum-fields

### -field OFFLINEFILES_PATHFILTER_SELF:0

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

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileseventsfilter-getpathfilter">IOfflineFilesEventsFilter::GetPathFilter</a>
