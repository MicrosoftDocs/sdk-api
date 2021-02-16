---
UID: NF:wmdmlog.IWMDMLogger.LogDword
title: IWMDMLogger::LogDword (wmdmlog.h)
description: The LogDword method logs a DWORD value to the current log file. A carriage return and line feed are added to each log entry.
helpviewer_keywords: ["IWMDMLogger interface [windows Media Device Manager]","LogDword method","IWMDMLogger.LogDword","IWMDMLogger::LogDword","IWMDMLoggerLogDword","LogDword","LogDword method [windows Media Device Manager]","LogDword method [windows Media Device Manager]","IWMDMLogger interface","wmdm.iwmdmlogger_logdword","wmdmlog/IWMDMLogger::LogDword"]
old-location: wmdm\iwmdmlogger_logdword.htm
tech.root: WMDM
ms.assetid: 68467750-76c5-4f2c-82cf-69c3db12fae9
ms.date: 12/05/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],LogDword method, IWMDMLogger.LogDword, IWMDMLogger::LogDword, IWMDMLoggerLogDword, LogDword, LogDword method [windows Media Device Manager], LogDword method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_logdword, wmdmlog/IWMDMLogger::LogDword
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
 - IWMDMLogger::LogDword
 - wmdmlog/IWMDMLogger::LogDword
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
 - IWMDMLogger.LogDword
---

# IWMDMLogger::LogDword


## -description

The <b>LogDword</b> method logs a <b>DWORD</b> value to the current log file. A carriage return and line feed are added to each log entry.

## -parameters

### -param dwFlags [in]

Flags that control the way a string is logged. This parameter is a combination of one or more of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_LOG_SEV_INFO</td>
<td>Tag the log entry as informational.</td>
</tr>
<tr>
<td>WMDM_LOG_SEV_WARN</td>
<td>Tag the log entry as a warning.</td>
</tr>
<tr>
<td>WMDM_LOG_SEV_ERROR</td>
<td>Tag the log entry as an error.</td>
</tr>
<tr>
<td>WMDM_LOG_NOTIMESTAMP</td>
<td>Do not include a time stamp on the log entry. Time stamps are in ISO format minus the time-zone information.</td>
</tr>
</table>

### -param pszSrcName [in]

Optional pointer to a string containing the name of the module that is making the log entry.

### -param pszLogFormat [in]

Pointer to a string that specifies the format of the log string. This string is of the same form as the format string for the <b>printf</b> function.

### -param dwLog [in]

<b>DWORD</b> value to log.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>