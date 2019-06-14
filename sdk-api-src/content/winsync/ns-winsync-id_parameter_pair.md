---
UID: NS:winsync._ID_PARAMETER_PAIR
title: ID_PARAMETER_PAIR (winsync.h)
author: windows-sdk-content
description: Represents the format of a synchronization entity ID.
old-location: winsync\id_parameter_pair.htm
tech.root: winsync
ms.assetid: f2b47196-8112-4f04-9944-a4a686d3c25c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID_PARAMETER_PAIR, ID_PARAMETER_PAIR structure [Windows Sync], winsync.id_parameter_pair, winsync/ID_PARAMETER_PAIR
ms.topic: struct
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - winsync.h
api_name:
 - ID_PARAMETER_PAIR
product: Windows
targetos: Windows
req.typenames: ID_PARAMETER_PAIR
req.redist: 
ms.custom: 19H1
---

# ID_PARAMETER_PAIR structure


## -description


Represents the format of a synchronization entity ID.


## -struct-fields




### -field fIsVariable

<b>TRUE</b> if the ID is variable length; otherwise, <b>FALSE</b>.


### -field cbIdSize

The length of the ID when <i>fIsVariable</i> is <b>FALSE</b>. The maximum length of the ID when <i>fIsVariable</i> is <b>TRUE</b>. Must be greater than zero.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/ns-winsync-_id_parameters">ID_PARAMETERS Structure</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-structures">Windows Sync Structures</a>
 

 

