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

# _REPAIR_COPIES_OUTPUT structure


## -description


Contains output of a repair copies operation returned from the 
     <a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a> control code.


## -struct-fields




### -field Size

Set to <code>sizeof(REPAIR_COPIES_OUTPUT)</code>.


### -field Status

Indicates the status of the repair operation. The value is a <b>NTSTATUS</b> value. 
      See 
      <a href="http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx">http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx</a> 
      for a list of <b>NTSTATUS</b> values.


### -field ResumeFileOffset

If the <b>Status</b> member indicates the operation was not successful, this is the 
      file offset to use to resume repair operations, skipping the range where errors were found.

