---
UID: NF:wmdmlog.IWMDMLogger.IsEnabled
title: IWMDMLogger::IsEnabled (wmdmlog.h)
description: The IsEnabled method determines whether logging is enabled.
helpviewer_keywords: ["IWMDMLogger interface [windows Media Device Manager]","IsEnabled method","IWMDMLogger.IsEnabled","IWMDMLogger::IsEnabled","IWMDMLoggerIsEnabled","IsEnabled","IsEnabled method [windows Media Device Manager]","IsEnabled method [windows Media Device Manager]","IWMDMLogger interface","wmdm.iwmdmlogger_isenabled","wmdmlog/IWMDMLogger::IsEnabled"]
old-location: wmdm\iwmdmlogger_isenabled.htm
tech.root: WMDM
ms.assetid: 10bf20bd-7457-4d37-82b5-7d761b4371c5
ms.date: 12/05/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],IsEnabled method, IWMDMLogger.IsEnabled, IWMDMLogger::IsEnabled, IWMDMLoggerIsEnabled, IsEnabled, IsEnabled method [windows Media Device Manager], IsEnabled method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_isenabled, wmdmlog/IWMDMLogger::IsEnabled
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
 - IWMDMLogger::IsEnabled
 - wmdmlog/IWMDMLogger::IsEnabled
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
 - IWMDMLogger.IsEnabled
---

# IWMDMLogger::IsEnabled


## -description

The <b>IsEnabled</b> method determines whether logging is enabled.

## -parameters

### -param pfEnabled [out]

Pointer to a flag that is true on output if logging is enabled.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

The file WmdmLog.idl is the IDL source code for WmdmLog.dll. This file is processed by the MIDL tool to produce the type library (WmdmLog.tlb) and marshaling code.


#### Examples


```cpp

// Create logging object.
CoCreateInstance(CLSID_WMDMLogger, NULL, CLSCTX_ALL, __uuidof(IWMDMLogger), (void**)&m_pLogger);
BOOL enabled = FALSE;
hr = m_pLogger->IsEnabled(&enabled);
// TODO: Display a message that logging is either enabled or disabled.
if(!enabled)
{
    if(m_pLogger->Enable(TRUE) != S_OK)
        m_pLogger = NULL;
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger">IWMDMLogger Interface</a>