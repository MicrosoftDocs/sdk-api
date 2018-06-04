---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMDMProgress::Begin


## -description



The <b>Begin</b> method indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.




## -parameters




### -param dwEstimatedTicks [in]

<b>DWORD</b> specifying the estimated number of ticks that are needed for the operation to complete.


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



This operation is called by various methods to indicate that an operation is beginning. The number of ticks passed in <i>dwEstimatedTicks</i> is an estimate of how many ticks are needed for the operation to complete. During the course of the operation, the <a href="https://msdn.microsoft.com/e85b6b46-2c42-461f-90b5-71b48bc4a111">Progress</a> method is called to indicate how many ticks have transpired. Applications can use the estimate to configure display mechanisms that show progress.

The <a href="https://msdn.microsoft.com/8c794aff-9800-405e-853a-56dd5bd84665">IWMDMProgress3::Begin3</a> method provides more information about what action is occurring.


#### Examples

The following C++ code is an implementation of the <b>Begin</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Begin(DWORD  dwEstimatedTicks)
{
    // TODO: Display the message: "IWMDMProgress::Begin called.: "
    // followed by the dwEstimatedTicks value.
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/8c794aff-9800-405e-853a-56dd5bd84665">IWMDMProgress3::Begin3</a>
 

 

