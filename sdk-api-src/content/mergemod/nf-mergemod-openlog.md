---
UID: NF:mergemod.OpenLog
title: OpenLog function
author: windows-driver-content
description: The OpenLog method of the Merge object opens a log file that receives progress and error messages. If the log file already exists, the installer appends new messages. If the log file does not exist, the installer creates a log file.
old-location: setup\merge_openlog.htm
old-project: Msi
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Merge class, OpenLog method, OpenLog, OpenLog method, OpenLog method, Merge class, _msi_openlog_method, setup.merge_openlog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mergemod.dll
api_name:
-	Merge.OpenLog
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# OpenLog function


## -description


The 
<b>OpenLog</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object opens a log file that receives progress and error messages. If the log file already exists, the installer appends new messages. If the log file does not exist, the installer creates a log file.


## -parameters




### -param Path

TBD




#### - Filename

Fully qualified file name pointing to a file to open or create.


## -returns



This method does not return a value.




## -remarks



Clients may send their own messages to this log file through the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406307">Log</a> method.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/b34e7f28-2cf3-4cc7-9a39-e1da6fb8c788">OpenLog</a> function.



