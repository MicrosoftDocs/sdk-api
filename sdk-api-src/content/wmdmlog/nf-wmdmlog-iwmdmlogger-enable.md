---
UID: NF:wmdmlog.IWMDMLogger.Enable
title: IWMDMLogger::Enable
author: windows-sdk-content
description: The Enable method enables or disables logging. Logging is enabled by default.
old-location: wmdm\iwmdmlogger_enable.htm
old-project: WMDM
ms.assetid: 6b0e48ff-ea34-4bcc-93e8-5ef0f5c39b06
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Enable, Enable method [windows Media Device Manager], Enable method [windows Media Device Manager],IWMDMLogger interface, IWMDMLogger interface [windows Media Device Manager],Enable method, IWMDMLogger.Enable, IWMDMLogger::Enable, IWMDMLoggerEnable, wmdm.iwmdmlogger_enable, wmdmlog/IWMDMLogger::Enable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmdmlog.h
req.include-header: 
req.redist: 
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
 - IWMDMLogger.Enable
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDMLogger::Enable


## -description



The <b>Enable</b> method enables or disables logging. Logging is enabled by default.




## -parameters




### -param fEnable [in]

Flag that enables logging if it is true and disables logging if it is <b>false</b>.


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
 

 

