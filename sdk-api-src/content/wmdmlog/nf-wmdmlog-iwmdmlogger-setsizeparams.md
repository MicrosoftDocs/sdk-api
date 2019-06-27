---
UID: NF:wmdmlog.IWMDMLogger.SetSizeParams
title: IWMDMLogger::SetSizeParams (wmdmlog.h)
author: windows-sdk-content
description: The SetSizeParams method sets the current size parameters for the current log file.
old-location: wmdm\iwmdmlogger_setsizeparams.htm
tech.root: WMDM
ms.assetid: f602efb8-7b00-4a9d-a61a-06e2f15e9185
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],SetSizeParams method, IWMDMLogger.SetSizeParams, IWMDMLogger::SetSizeParams, IWMDMLoggerSetSizeParams, SetSizeParams, SetSizeParams method [windows Media Device Manager], SetSizeParams method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_setsizeparams, wmdmlog/IWMDMLogger::SetSizeParams
ms.topic: method
f1_keywords: 
 - "wmdmlog/IWMDMLogger.SetSizeParams"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMLogger.SetSizeParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMLogger::SetSizeParams


## -description



The <b>SetSizeParams</b> method sets the current size parameters for the current log file.




## -parameters




### -param dwMaxSize [in]

The approximate maximum size of the log file. The size of the log file is checked before each log entry is made. Therefore, the log file can grow bigger than the maximum size until the next log entry is made.


### -param dwShrinkToSize [in]

The approximate file size to which the log file should be reduced when the maximum log file size is reached. The log file is generally shrunk to a little smaller than this value so that the file is not split in the middle of a log entry.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/error-codes">Error Codes</a>.

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>
 

 

