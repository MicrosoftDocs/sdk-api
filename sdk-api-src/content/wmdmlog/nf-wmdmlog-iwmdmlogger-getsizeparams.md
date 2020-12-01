---
UID: NF:wmdmlog.IWMDMLogger.GetSizeParams
title: IWMDMLogger::GetSizeParams (wmdmlog.h)
description: The GetSizeParams method retrieves the current size parameters of the current log file.
helpviewer_keywords: ["GetSizeParams","GetSizeParams method [windows Media Device Manager]","GetSizeParams method [windows Media Device Manager]","IWMDMLogger interface","IWMDMLogger interface [windows Media Device Manager]","GetSizeParams method","IWMDMLogger.GetSizeParams","IWMDMLogger::GetSizeParams","IWMDMLoggerGetSizeParams","wmdm.iwmdmlogger_getsizeparams","wmdmlog/IWMDMLogger::GetSizeParams"]
old-location: wmdm\iwmdmlogger_getsizeparams.htm
tech.root: WMDM
ms.assetid: c8775cea-3764-44cf-a977-c4c529e2133e
ms.date: 12/05/2018
ms.keywords: GetSizeParams, GetSizeParams method [windows Media Device Manager], GetSizeParams method [windows Media Device Manager],IWMDMLogger interface, IWMDMLogger interface [windows Media Device Manager],GetSizeParams method, IWMDMLogger.GetSizeParams, IWMDMLogger::GetSizeParams, IWMDMLoggerGetSizeParams, wmdm.iwmdmlogger_getsizeparams, wmdmlog/IWMDMLogger::GetSizeParams
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
 - IWMDMLogger::GetSizeParams
 - wmdmlog/IWMDMLogger::GetSizeParams
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
 - IWMDMLogger.GetSizeParams
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>