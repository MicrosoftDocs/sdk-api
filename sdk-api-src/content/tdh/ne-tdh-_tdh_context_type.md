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

# _TDH_CONTEXT_TYPE enumeration


## -description



		Defines the context type.
		
		
	
	


## -enum-fields




### -field TDH_CONTEXT_WPP_TMFFILE

Null-terminated Unicode string that contains the name of the .tmf file used for parsing the WPP log. Typically, the .tmf file name is picked up from the event GUID so you do not have to specify the file name.


### -field TDH_CONTEXT_WPP_TMFSEARCHPATH

Null-terminated Unicode string that contains the path to the .tmf file. You do not have to specify this path if the search path contains the file. Only specify this context information if you also specify the TDH_CONTEXT_WPP_TMFFILE context type. If the file is not found, TDH searches the following locations in the given order:

<ul>
<li>The path specified in the TRACE_FORMAT_SEARCH_PATH environment variable</li>
<li>The current folder</li>
</ul>

### -field TDH_CONTEXT_WPP_GMT

A 1-byte Boolean flag that indicates if the WPP event time stamp should be converted to Universal Time Coordinate (UTC). If 1, the time stamp is converted to UTC. If 0, the time stamp is in local time. By default, the time stamp is in local time. 


### -field TDH_CONTEXT_POINTERSIZE

Size, in bytes, of the pointer data types or size_t data types used in the event. Indicates if the event used 4-byte or 8-byte values. By default, the pointer size is the pointer size of the decoding computer.

To determine the size of the pointer or size_t value, use the <b>PointerSize</b> member of  <a href="https://msdn.microsoft.com/13fdabe6-c904-4546-b876-c145f6a6c345">TRACE_LOGFILE_HEADER</a> (the first event you receive in your <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback contains this header in the data section). However, this value may not be accurate. For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set <b>PointerSize</b> to 8.


### -field TDH_CONTEXT_PDB_PATH

Null-terminated Unicode string that contains the name of the .pdb file for the binary that contains WPP messages. This parameter can be used as an alternative to <b>TDH_CONTEXT_WPP_TMFFILE</b> or <b>TDH_CONTEXT_WPP_TMFSEARCHPATH</b>.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field TDH_CONTEXT_MAXIMUM

Reserved.


## -remarks



If you are specifying context information for a legacy ETW event, you only need to specify the TDH_CONTEXT_POINTERSIZE type—the other types are used for WPP events and are ignored for legacy ETW events.




## -see-also




<a href="https://msdn.microsoft.com/184df0af-3ac5-406f-a298-4f23826ad85e">TDH_CONTEXT</a>
 

 

