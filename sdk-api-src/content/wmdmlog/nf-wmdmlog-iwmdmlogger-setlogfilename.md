---
UID: NF:wmdmlog.IWMDMLogger.SetLogFileName
title: IWMDMLogger::SetLogFileName (wmdmlog.h)
description: The SetLogFileName method sets the full path to the current log file. All subsequent log entries will be placed in this file.
helpviewer_keywords: ["IWMDMLogger interface [windows Media Device Manager]","SetLogFileName method","IWMDMLogger.SetLogFileName","IWMDMLogger::SetLogFileName","IWMDMLoggerSetLogFileName","SetLogFileName","SetLogFileName method [windows Media Device Manager]","SetLogFileName method [windows Media Device Manager]","IWMDMLogger interface","wmdm.iwmdmlogger_setlogfilename","wmdmlog/IWMDMLogger::SetLogFileName"]
old-location: wmdm\iwmdmlogger_setlogfilename.htm
tech.root: WMDM
ms.assetid: 9ceecf17-01b4-4461-9ca7-229704c5916c
ms.date: 12/05/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],SetLogFileName method, IWMDMLogger.SetLogFileName, IWMDMLogger::SetLogFileName, IWMDMLoggerSetLogFileName, SetLogFileName, SetLogFileName method [windows Media Device Manager], SetLogFileName method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_setlogfilename, wmdmlog/IWMDMLogger::SetLogFileName
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMLogger::SetLogFileName
 - wmdmlog/IWMDMLogger::SetLogFileName
dev_langs:
 - c++
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The default log file is &lt; <i>Windows directory</i> &gt;\System32\Wmdm.log.

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>