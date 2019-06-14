---
UID: NF:gpmgmt.IGPMMigrationTable.GetEntry
title: IGPMMigrationTable::GetEntry (gpmgmt.h)
author: windows-sdk-content
description: The GetEntry method gets the entry in the migration table for a specified source field.
old-location: gpmc\igpmmigrationtable_getentry.htm
tech.root: gpmc
ms.assetid: 3d6985ab-dbea-446c-9666-5fa19b97b40c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMMigrationTable class [GPMC],GetEntry method, GetEntry, GetEntry method [GPMC], GetEntry method [GPMC],GPMMigrationTable class, GetEntry method [GPMC],IGPMMigrationTable interface, IGPMMigrationTable interface [GPMC],GetEntry method, IGPMMigrationTable.GetEntry, IGPMMigrationTable::GetEntry, gpmc.igpmmigrationtable_getentry, gpmgmt/IGPMMigrationTable::GetEntry
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.GetEntry
 - GPMMigrationTable.GetEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMMigrationTable::GetEntry


## -description


The <b>GetEntry</b> method gets the entry in the migration table for a specified source field.


## -parameters




### -param bstrSource [in]

Source field of the entry to retrieve.


### -param ppEntry [out]

A pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentry">IGPMMapEntry</a> interface.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentry">GPMMapEntry</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentry">GPMMapEntry</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMMigrationTable</a>
 

 

