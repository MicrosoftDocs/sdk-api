---
UID: NS:winsync._ID_PARAMETER_PAIR
title: "_ID_PARAMETER_PAIR"
author: windows-sdk-content
description: Represents the format of a synchronization entity ID.
old-location: winsync\id_parameter_pair.htm
old-project: winsync
ms.assetid: f2b47196-8112-4f04-9944-a4a686d3c25c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ID_PARAMETER_PAIR, ID_PARAMETER_PAIR structure [Windows Sync], _ID_PARAMETER_PAIR, winsync.id_parameter_pair, winsync/ID_PARAMETER_PAIR
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ID_PARAMETER_PAIR
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ID_PARAMETER_PAIR structure


## -description


Represents the format of a synchronization entity ID.


## -struct-fields




### -field fIsVariable

<b>TRUE</b> if the ID is variable length; otherwise, <b>FALSE</b>.


### -field cbIdSize

The length of the ID when <i>fIsVariable</i> is <b>FALSE</b>. The maximum length of the ID when <i>fIsVariable</i> is <b>TRUE</b>. Must be greater than zero.


## -see-also




<a href="https://msdn.microsoft.com/7391689a-5546-409a-9fff-2ceced1850fe">ID_PARAMETERS Structure</a>



<a href="https://msdn.microsoft.com/eed33384-f8bd-4a3a-8d04-b59c534f9114">Windows Sync Structures</a>
 

 

