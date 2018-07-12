---
UID: NF:wmdmlog.IWMDMLogger.IsEnabled
title: IWMDMLogger::IsEnabled
author: windows-sdk-content
description: The IsEnabled method determines whether logging is enabled.
old-location: wmdm\iwmdmlogger_isenabled.htm
old-project: WMDM
ms.assetid: 10bf20bd-7457-4d37-82b5-7d761b4371c5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMLogger interface [windows Media Device Manager],IsEnabled method, IWMDMLogger.IsEnabled, IWMDMLogger::IsEnabled, IWMDMLoggerIsEnabled, IsEnabled, IsEnabled method [windows Media Device Manager], IsEnabled method [windows Media Device Manager],IWMDMLogger interface, wmdm.iwmdmlogger_isenabled, wmdmlog/IWMDMLogger::IsEnabled
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
 - IWMDMLogger.IsEnabled
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The file WmdmLog.idl is the IDL source code for WmdmLog.dll. This file is processed by the MIDL tool to produce the type library (WmdmLog.tlb) and marshaling code.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Create logging object.
CoCreateInstance(CLSID_WMDMLogger, NULL, CLSCTX_ALL, __uuidof(IWMDMLogger), (void**)&amp;m_pLogger);
BOOL enabled = FALSE;
hr = m_pLogger-&gt;IsEnabled(&amp;enabled);
// TODO: Display a message that logging is either enabled or disabled.
if(!enabled)
{
    if(m_pLogger-&gt;Enable(TRUE) != S_OK)
        m_pLogger = NULL;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad">Enabling Logging</a>



<a href="https://msdn.microsoft.com/bededb91-f343-455b-a3ef-548e6f961933">IWMDMLogger Interface</a>
 

 

