---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0002
title: FileFormat
author: windows-sdk-content
description: Defines the format of the data in the log file.
old-location: pla\fileformat.htm
tech.root: pla
ms.assetid: 8ec50a96-0c8c-401a-8849-e3753fe15952
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FileFormat, FileFormat enumeration [PLA], base.fileformat, pla.fileformat, pla/FileFormat, pla/plaBinary, pla/plaCommaSeparated, pla/plaSql, pla/plaTabSeparated, plaBinary, plaCommaSeparated, plaSql, plaTabSeparated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Pla.h
api_name:
 - FileFormat
product: Windows
targetos: Windows
req.typenames: FileFormat
req.redist: 
---

# FileFormat enumeration


## -description


Defines the format of the data in the log file.


## -enum-fields




### -field plaCommaSeparated

Comma-separated log file. The first line in the text file contains column headings followed by comma-separated data in the remaining lines of the log file. 


### -field plaTabSeparated

Tab-separated log file. The first line in the text file contains column headings followed by tab-separated data in the remaining lines of the log file. 


### -field plaSql

The log contains SQL records. 


### -field plaBinary

Binary log file. 


## -see-also




<a href="https://msdn.microsoft.com/3b980ea6-cb08-4e10-b4b3-40fd504d5e8f">IPerformanceCounterDataCollector::LogFileFormat</a>
 

 

