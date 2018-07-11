---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0008
title: "__MIDL___MIDL_itf_winsync_0000_0000_0008"
author: windows-sdk-content
description: Indicates the type of information that is included in a change batch during filtered synchronization.
old-location: winsync\filtering_type.htm
old-project: winsync
ms.assetid: 6bcbc011-9d47-4c88-a62e-0c9366abc7d3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: FILTERING_TYPE, FILTERING_TYPE enumeration [Windows Sync], FT_CURRENT_ITEMS_ONLY, __MIDL___MIDL_itf_winsync_0000_0000_0008, winsync.filtering_type, winsync/FILTERING_TYPE, winsync/FT_CURRENT_ITEMS_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: FILTERING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - FILTERING_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __MIDL___MIDL_itf_winsync_0000_0000_0008 enumeration


## -description


Indicates the type of information that is included in a change batch during filtered synchronization.




## -enum-fields




### -field FT_CURRENT_ITEMS_ONLY

The change batch includes data and metadata for items that are currently in the filter.



### -field FT_CURRENT_ITEMS_AND_VERSIONS_FOR_MOVED_OUT_ITEMS




## -remarks



A replica that does not keep ghosts for items that are not in the filter indicates this by using <b>FT_CURRENT_ITEMS_ONLY</b>.

<div class="alert"><b>Note</b>  An item that is excluded by the filter in one replica, but is still tracked in the other replica is known as a "ghost".</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

