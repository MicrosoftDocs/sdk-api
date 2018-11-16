---
UID: NN:wmdmlog.IWMDMLogger
title: IWMDMLogger
author: windows-sdk-content
description: The IWMDMLogger interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file.
old-location: wmdm\iwmdmlogger.htm
tech.root: WMDM
ms.assetid: bededb91-f343-455b-a3ef-548e6f961933
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMDMLogger, IWMDMLogger interface [windows Media Device Manager], IWMDMLogger interface [windows Media Device Manager],described, IWMDMLoggerInterface, wmdm.iwmdmlogger, wmdmlog/IWMDMLogger
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMLogger interface


## -description



The <b>IWMDMLogger</b> interface is used by Windows Media Device Manager applications and service providers to log entries in a common log file. Components do not need to be certified to use this object.

This interface is exposed by a COM object that must be created using the class ID CLSID_WMDMLogger, as shown here:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IWMDMLogger* m_pLogger = NULL;
CoCreateInstance(CLSID_WMDMLogger, NULL, CLSCTX_ALL, __uuidof(IWMDMLogger), (void**)&amp;m_pLogger);
</pre>
</td>
</tr>
</table></span></div>
This interface GUID is not properly defined in mssachlp.lib; therefore, to get the proper definitions when implementing this interface, you must #include both mswmdm.h and wmdmlog_i.c from wmdmlog.idl.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMLogger</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMLogger</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6b0e48ff-ea34-4bcc-93e8-5ef0f5c39b06">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables logging.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/094761e6-539c-43ca-b882-f3dd7a19a243">GetLogFileName</a>
</td>
<td align="left" width="63%">
Returns the full path to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8775cea-3764-44cf-a977-c4c529e2133e">GetSizeParams</a>
</td>
<td align="left" width="63%">
Retrieves the current size parameters of the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10bf20bd-7457-4d37-82b5-7d761b4371c5">IsEnabled</a>
</td>
<td align="left" width="63%">
Determines whether logging is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68467750-76c5-4f2c-82cf-69c3db12fae9">LogDword</a>
</td>
<td align="left" width="63%">
Logs a <b>DWORD</b> value to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a084ef6-20dc-4363-b9b8-c4e9bcb1dd71">LogString</a>
</td>
<td align="left" width="63%">
Logs a string to the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b26aede-0db4-4597-8494-7fd5e5cba857">Reset</a>
</td>
<td align="left" width="63%">
Deletes the contents of the current log file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ceecf17-01b4-4461-9ca7-229704c5916c">SetLogFileName</a>
</td>
<td align="left" width="63%">
Sets the full path to the current log file. All subsequent log entries are placed in this file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f602efb8-7b00-4a9d-a61a-06e2f15e9185">SetSizeParams</a>
</td>
<td align="left" width="63%">
Sets the current size parameters for the current log file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad">Enabling Logging</a>



<a href="https://msdn.microsoft.com/2d1abf2b-29d0-49b0-ae79-f07a35c42265">Interfaces for Service Providers and Applications</a>
 

 

