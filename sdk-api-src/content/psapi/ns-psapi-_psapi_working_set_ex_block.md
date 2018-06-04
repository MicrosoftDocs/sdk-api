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

# _PSAPI_WORKING_SET_EX_BLOCK structure


## -description


Contains extended working set information for a page.


## -struct-fields




### -field Flags

The working set information. See the description of the structure  members for information about the layout 
      of this variable.


### -field Valid

If this bit is 1, the subsequent members are valid; otherwise they should be ignored.


### -field ShareCount

The number of processes that share this page. The maximum value of this member is 7.


### -field Win32Protection

The memory protection attributes of the page. For a list of values, see
       <a href="https://msdn.microsoft.com/09839db7-2118-4a7d-a707-a08c92bd600c">Memory Protection Constants</a>.


### -field Shared

If this bit is 1, the page can be shared.


### -field Node

The NUMA node. The maximum value of this member is 63.


### -field Locked

If this bit is 1, the virtual page is locked in physical memory.


### -field LargePage

If this bit is 1, the page is a large page.


### -field Reserved

Reserved.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.


### -field Bad

If this bit is 1, the page is has been reported as bad.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.


### -field ReservedUlong

Reserved. This member is only available on 64-bit code running on 64-bit editions of Windows.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.


### -field Invalid

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This structure is not available before Windows Server 2012 and Windows 8.


### -field Invalid.Valid

If this bit is 0, the subsequent members are valid; otherwise they should be ignored.


### -field Invalid.Reserved0

Reserved.


### -field Invalid.Shared

If this bit is 1, the page can be shared.


### -field Invalid.Reserved1

Reserved.


### -field Invalid.Bad

If this bit is 1, the page is has been reported as bad.


### -field Invalid.ReservedUlong

Reserved. This member is only available on 64-bit code running on 64-bit editions of Windows.


## -see-also




<a href="https://msdn.microsoft.com/08e53ebf-f694-46ad-b8b7-3dc179ab80ff">PSAPI Structures</a>



<a href="https://msdn.microsoft.com/d3500737-b9af-41a8-bf69-61d0bfbd6ce4">PSAPI_WORKING_SET_EX_INFORMATION</a>



<a href="https://msdn.microsoft.com/59ae76c9-e954-4648-9c9f-787136375b02">QueryWorkingSetEx</a>
 

 

