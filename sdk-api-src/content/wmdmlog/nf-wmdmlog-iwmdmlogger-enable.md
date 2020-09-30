---
UID: NF:wmdmlog.IWMDMLogger.Enable
title: IWMDMLogger::Enable (wmdmlog.h)
description: The Enable method enables or disables logging. Logging is enabled by default.
helpviewer_keywords: ["Enable","Enable method [windows Media Device Manager]","Enable method [windows Media Device Manager]","IWMDMLogger interface","IWMDMLogger interface [windows Media Device Manager]","Enable method","IWMDMLogger.Enable","IWMDMLogger::Enable","IWMDMLoggerEnable","wmdm.iwmdmlogger_enable","wmdmlog/IWMDMLogger::Enable"]
old-location: wmdm\iwmdmlogger_enable.htm
tech.root: WMDM
ms.assetid: 6b0e48ff-ea34-4bcc-93e8-5ef0f5c39b06
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [windows Media Device Manager], Enable method [windows Media Device Manager],IWMDMLogger interface, IWMDMLogger interface [windows Media Device Manager],Enable method, IWMDMLogger.Enable, IWMDMLogger::Enable, IWMDMLoggerEnable, wmdm.iwmdmlogger_enable, wmdmlog/IWMDMLogger::Enable
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
 - IWMDMLogger::Enable
 - wmdmlog/IWMDMLogger::Enable
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
 - IWMDMLogger.Enable
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>