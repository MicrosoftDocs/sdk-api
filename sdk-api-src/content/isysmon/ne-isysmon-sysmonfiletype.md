---
UID: NE:isysmon.__MIDL___MIDL_itf_sysmon_0000_0000_0001
title: SysmonFileType (isysmon.h)
description: Determines the format in which the counter data is saved to a file.
helpviewer_keywords: ["SysmonFileType","SysmonFileType enumeration [SysMon]","base.sysmonfiletype","isysmon/SysmonFileType","isysmon/sysmonFileBlg","isysmon/sysmonFileCsv","isysmon/sysmonFileGif","isysmon/sysmonFileHtml","isysmon/sysmonFileReport","isysmon/sysmonFileRetiredBlg","isysmon/sysmonFileTsv","sysmon.sysmonfiletype","sysmonFileBlg","sysmonFileCsv","sysmonFileGif","sysmonFileHtml","sysmonFileReport","sysmonFileRetiredBlg","sysmonFileTsv"]
old-location: sysmon\sysmonfiletype.htm
tech.root: SysMon
ms.assetid: a3db8565-6316-445e-8fb2-b0bfb08bf72c
ms.date: 12/05/2018
ms.keywords: SysmonFileType, SysmonFileType enumeration [SysMon], base.sysmonfiletype, isysmon/SysmonFileType, isysmon/sysmonFileBlg, isysmon/sysmonFileCsv, isysmon/sysmonFileGif, isysmon/sysmonFileHtml, isysmon/sysmonFileReport, isysmon/sysmonFileRetiredBlg, isysmon/sysmonFileTsv, sysmon.sysmonfiletype, sysmonFileBlg, sysmonFileCsv, sysmonFileGif, sysmonFileHtml, sysmonFileReport, sysmonFileRetiredBlg, sysmonFileTsv
f1_keywords:
- isysmon/SysmonFileType
dev_langs:
- c++
req.header: isysmon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- ISysmon.h
api_name:
- SysmonFileType
targetos: Windows
req.typenames: SysmonFileType
req.redist: 
ms.custom: 19H1
---

# SysmonFileType enumeration


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




<a href="https://docs.microsoft.com/windows/desktop/SysMon/systemmonitor-relog">SystemMonitor.Relog</a>



<a href="https://docs.microsoft.com/windows/desktop/SysMon/systemmonitor-saveas">SystemMonitor.SaveAs</a>
 

 

