---
UID: NN:wmdmlog.IWMDMLogger
title: IWMDMLogger (wmdmlog.h)
description: The IWMDMLogger interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file.
helpviewer_keywords: ["IWMDMLogger","IWMDMLogger interface [windows Media Device Manager]","IWMDMLogger interface [windows Media Device Manager]","described","IWMDMLoggerInterface","wmdm.iwmdmlogger","wmdmlog/IWMDMLogger"]
old-location: wmdm\iwmdmlogger.htm
tech.root: WMDM
ms.assetid: bededb91-f343-455b-a3ef-548e6f961933
ms.date: 12/05/2018
ms.keywords: IWMDMLogger, IWMDMLogger interface [windows Media Device Manager], IWMDMLogger interface [windows Media Device Manager],described, IWMDMLoggerInterface, wmdm.iwmdmlogger, wmdmlog/IWMDMLogger
f1_keywords:
- wmdmlog/IWMDMLogger
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmdmlog.h
api_name:
- IWMDMLogger
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMLogger interface


## -description



The <b>IWMDMLogger</b> interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file. Components do not need to be certified to use this object.

This interface is exposed by a COM object that must be created using the class ID CLSID_WMDMLogger, as shown here:


```cpp

IWMDMLogger* m_pLogger = NULL;
CoCreateInstance(CLSID_WMDMLogger, NULL, CLSCTX_ALL, __uuidof(IWMDMLogger), (void**)&m_pLogger);

```


This interface GUID is not properly defined in mssachlp.lib; therefore, to get the proper definitions when implementing this interface, you must #include both mswmdm.h and wmdmlog_i.c from wmdmlog.idl.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMLogger</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMLogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMLogger</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-getlogfilename">GetLogFileName</a>
</td>
<td align="left" width="63%">
Returns the full path to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-getsizeparams">GetSizeParams</a>
</td>
<td align="left" width="63%">
Retrieves the current size parameters of the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled">IsEnabled</a>
</td>
<td align="left" width="63%">
Determines whether logging is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword">LogDword</a>
</td>
<td align="left" width="63%">
Logs a <b>DWORD</b> value to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring">LogString</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset">Reset</a>
</td>
<td align="left" width="63%">
Deletes the contents of the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename">SetLogFileName</a>
</td>
<td align="left" width="63%">
Sets the full path to the current log file. All subsequent log entries are placed in this file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams">SetSizeParams</a>
</td>
<td align="left" width="63%">
Sets the current size parameters for the current log file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/enabling-logging">Enabling Logging</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers-and-applications">Interfaces for Service Providers and Applications</a>
 

 

