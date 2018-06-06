---
UID: NF:wmdmlog.IWMDMLogger.SetLogFileName
title: IWMDMLogger::SetLogFileName
author: windows-sdk-content
description: The SetLogFileName method sets the full path to the current log file. All subsequent log entries will be placed in this file.
old-location: wmdm\iwmdmlogger_setlogfilename.htm
old-project: WMDM
ms.assetid: 9ceecf17-01b4-4461-9ca7-229704c5916c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],SetLogFileName method, IWMDMLogger.SetLogFileName, IWMDMLogger::SetLogFileName, IWMDMLoggerSetLogFileName, SetLogFileName, SetLogFileName method [windows Media Device Manager], SetLogFileName method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_setlogfilename, wmdmlog/IWMDMLogger::SetLogFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmdmlog.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: ASF_INDEX_IDENTIFIER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMLogger.SetLogFileName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDMLogger::SetLogFileName


## -description



The <b>SetLogFileName</b> method sets the full path to the current log file. All subsequent log entries will be placed in this file.




## -parameters




### -param pszFilename [in]

Pointer to a string that is the full path to the new log file. Note that this is not a wide-character string.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The default log file is &lt; <i>Windows directory</i> &gt;\System32\Wmdm.log.




## -see-also




<a href="https://msdn.microsoft.com/50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad">Enabling Logging</a>



<a href="https://msdn.microsoft.com/bededb91-f343-455b-a3ef-548e6f961933">IWMDMLogger Interface</a>
 

 

