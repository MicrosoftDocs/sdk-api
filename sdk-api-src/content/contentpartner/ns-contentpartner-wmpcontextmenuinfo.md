---
UID: NS:contentpartner.WMPContextMenuInfo
title: WMPContextMenuInfo (contentpartner.h)
author: windows-sdk-content
description: The WMPContextMenuInfo structure contains data about a context menu command.
old-location: wmp\wmpcontextmenuinfo.htm
tech.root: WMP
ms.assetid: a37ddbe1-7c66-4060-b93d-bd494cdc4521
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMPContextMenuInfo, WMPContextMenuInfo structure [Windows Media Player], contentpartner/WMPContextMenuInfo, wmp.wmpcontextmenuinfo
ms.topic: struct
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - contentpartner.h
api_name:
 - WMPContextMenuInfo
product: Windows
targetos: Windows
req.typenames: WMPContextMenuInfo
req.redist: 
---

# WMPContextMenuInfo structure


## -description


The <b>WMPContextMenuInfo</b> structure contains data about a context menu command.
<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div><div> </div>

## -struct-fields




### -field dwID

The ID of the command.


### -field bstrMenuText

The menu text to display for the command.


### -field bstrHelpText

The help text to display for the command.


## -remarks



This structure is retrieved by a call to <a href="https://msdn.microsoft.com/en-us/library/Dd563163(v=VS.85).aspx">IWMPContentPartner::GetCommands</a>.




## -see-also




<a href="https://msdn.microsoft.com/e1aff1a3-cf24-4292-afcd-92e77b178a3a">Structures for Type 1 Online Stores</a>
 

 

