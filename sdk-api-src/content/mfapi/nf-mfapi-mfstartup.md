---
UID: NF:mfapi.MFStartup
title: MFStartup function (mfapi.h)
author: windows-sdk-content
description: Initializes Microsoft Media Foundation.
old-location: mf\mfstartup.htm
tech.root: medfound
ms.assetid: b4472e40-3681-4b26-9385-4df7bf19c2d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFStartup, MFStartup function [Media Foundation], b4472e40-3681-4b26-9385-4df7bf19c2d8, mf.mfstartup, mfapi/MFStartup
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFStartup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFStartup function


## -description


Initializes Microsoft Media Foundation.


## -parameters




### -param Version

Version number. Use the value <b>MF_VERSION</b>, defined in mfapi.h.


### -param dwFlags

This parameter is optional when using C++ but required in C. The value must be one of the following flags:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MFSTARTUP_NOSOCKET</dt>
</dl>
</td>
<td width="60%">
Do not initialize the sockets library.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MFSTARTUP_LITE</dt>
</dl>
</td>
<td width="60%">
Equivalent to MFSTARTUP_NOSOCKET.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MFSTARTUP_FULL</dt>
</dl>
</td>
<td width="60%">
Initialize the entire Media Foundation platform. This is the default value when <i>dwFlags</i> is not specified.
              

</td>
</tr>
</table>
 


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BAD_STARTUP_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The <i>Version</i> parameter requires a newer version of Media Foundation than the version that is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_DISABLED_IN_SAFEMODE</b></dt>
</dl>
</td>
<td width="60%">
The Media Foundation platform is disabled because the system was started in "Safe Mode" (fail-safe boot).
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Media Foundation is not implemented on the system.  This error can occur if the media components are not present (See <a href="http://support.microsoft.com/kb/2703761">KB2703761</a> for more info). 

</td>
</tr>
</table>
 




## -remarks



An application must call this function before using Media Foundation. Before your application quits, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> once for every previous call to <b>MFStartup</b>.
      

Do not call <b>MFStartup</b> or <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> from work queue threads. For more information about work queues, see <a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

#### Examples


```cpp
    hr = MFStartup(MF_VERSION);

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/initializing-media-foundation">Initializing Media Foundation</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

