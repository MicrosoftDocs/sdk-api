---
UID: NF:wmdmlog.IWMDMLogger.GetLogFileName
title: IWMDMLogger::GetLogFileName
author: windows-sdk-content
description: The GetLogFileName method returns the full path to the current log file.
old-location: wmdm\iwmdmlogger_getlogfilename.htm
old-project: WMDM
ms.assetid: 094761e6-539c-43ca-b882-f3dd7a19a243
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetLogFileName, GetLogFileName method [windows Media Device Manager], GetLogFileName method [windows Media Device Manager],IWMDMLogger interface, IWMDMLogger interface [windows Media Device Manager],GetLogFileName method, IWMDMLogger.GetLogFileName, IWMDMLogger::GetLogFileName, IWMDMLoggerGetLogFileName, wmdm.iwmdmlogger_getlogfilename, wmdmlog/IWMDMLogger::GetLogFileName
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
req.typenames: ASF_INDEX_IDENTIFIER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMLogger.GetLogFileName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDMLogger::GetLogFileName


## -description



The <b>GetLogFileName</b> method returns the full path to the current log file.




## -parameters




### -param pszFilename [out]

Pointer to a buffer to receive the log file name.


### -param nMaxChars [in]

Specifies the size of the <i>pszFilename</i> buffer. This is the maximum number of characters that can be placed in the buffer, including the terminating <b>NULL</b> character.


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
 

 

