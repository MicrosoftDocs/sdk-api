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

# __MIDL___MIDL_itf_sysmon_0000_0000_0001 enumeration


## -description


Determines the format in which the counter data is saved to a file.


## -enum-fields




### -field sysmonFileHtml

Saves the control's property settings, list of counters, and counter data as HTML to a file. If the source of the counter data is a log file, the counter data is not saved.


### -field sysmonFileReport

Saves the counter data displayed in the report view as tab-separated data to a file. If the counter data is displayed in the graph view, only the last sampled counter data is saved to the file.


### -field sysmonFileCsv

Saves the counter data as comma-separated data to a file.


### -field sysmonFileTsv

Saves the counter data as tab-separated data to a file.


### -field sysmonFileBlg

Saves the counter data as binary data to a file.


### -field sysmonFileRetiredBlg

Saves the counter data in the Windows 2000 binary format to a file.


### -field sysmonFileGif

Saves the image of the System Monitor control to a file. The image does not include the toolbar, if enabled.


## -see-also




<a href="https://msdn.microsoft.com/4439f9ef-99e0-47d4-8f6f-d08afcba672d">SystemMonitor.Relog</a>



<a href="https://msdn.microsoft.com/34824c54-d8f4-4c2b-b417-aa0914c7164b">SystemMonitor.SaveAs</a>
 

 

