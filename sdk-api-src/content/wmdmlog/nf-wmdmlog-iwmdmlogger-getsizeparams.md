---
UID: NF:wmdmlog.IWMDMLogger.GetSizeParams
title: IWMDMLogger::GetSizeParams
author: windows-sdk-content
description: The GetSizeParams method retrieves the current size parameters of the current log file.
old-location: wmdm\iwmdmlogger_getsizeparams.htm
tech.root: WMDM
ms.assetid: c8775cea-3764-44cf-a977-c4c529e2133e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSizeParams, GetSizeParams method [windows Media Device Manager], GetSizeParams method [windows Media Device Manager],IWMDMLogger interface, IWMDMLogger interface [windows Media Device Manager],GetSizeParams method, IWMDMLogger.GetSizeParams, IWMDMLogger::GetSizeParams, IWMDMLoggerGetSizeParams, wmdm.iwmdmlogger_getsizeparams, wmdmlog/IWMDMLogger::GetSizeParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMDMLogger.GetSizeParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMLogger::GetSizeParams


## -description



The <b>GetSizeParams</b> method retrieves the current size parameters of the current log file.




## -parameters




### -param pdwMaxSize [out]

Pointer to a buffer that receives the approximate maximum size of the log file. This parameter can be <b>NULL</b>.


### -param pdwShrinkToSize [out]

Pointer to a buffer that receives the approximate size to which the log file will be reduced after it reaches the maximum size. This parameter can be <b>NULL</b>.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad">Enabling Logging</a>



<a href="https://msdn.microsoft.com/bededb91-f343-455b-a3ef-548e6f961933">IWMDMLogger Interface</a>
 

 

