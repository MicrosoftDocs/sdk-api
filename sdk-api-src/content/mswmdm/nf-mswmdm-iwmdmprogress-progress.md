---
UID: NF:mswmdm.IWMDMProgress.Progress
title: IWMDMProgress::Progress
author: windows-sdk-content
description: The Progress method indicates that an operation is still in progress.
old-location: wmdm\iwmdmprogress_progress.htm
tech.root: WMDM
ms.assetid: e85b6b46-2c42-461f-90b5-71b48bc4a111
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMProgress interface [windows Media Device Manager],Progress method, IWMDMProgress.Progress, IWMDMProgress::Progress, IWMDMProgressProgress, Progress, Progress method [windows Media Device Manager], Progress method [windows Media Device Manager],IWMDMProgress interface, mswmdm/IWMDMProgress::Progress, wmdm.iwmdmprogress_progress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mswmdm.h
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
 - IWMDMProgress.Progress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMProgress::Progress


## -description



The <b>Progress</b> method indicates that an operation is still in progress.




## -parameters




### -param dwTranspiredTicks [in]

<b>DWORD</b> specifying the number of ticks that have transpired so far.


## -returns



The application should return one of the following <b>HRESULT</b> values.

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
The operation should continue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_USER_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager should cancel the current operation without waiting for it to finish. If the application is using block mode, then Windows Media Device Manager will return this error to the application.

</td>
</tr>
</table>
 




## -remarks



This method is called by all other Windows Media Device Manager methods. The intention is that <b>Progress</b> will be called once per estimated tick. However, the <i>dwTranspiredTicks</i> parameter must be checked on each call because the operation being performed may not guarantee a call once for each estimated tick.

The application returns S_OK to the calling method to indicate that the operation should continue. The application returns WMDM_E_USER_CANCELLED to indicate that the operation should be cancelled. If the application is using block mode and returns WMDM_E_USER_CANCELLED, then Windows Media Device Manager will return this same error to the application.


#### Examples

The following C++ code is a simple implementation of the <b>Progress</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Progress(DWORD  dwTranspiredTicks)
{
    // TODO: Display the message: "IWMDMProgress::Progress called" 
    // followed by the dwTranspiredTicks value.
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/33f1de9c-f2eb-4b83-89a1-404a8c50ee08">IWMDMProgress3::Progress3</a>
 

 

