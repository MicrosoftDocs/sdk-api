---
UID: NF:mswmdm.IWMDMProgress.Begin
title: IWMDMProgress::Begin
author: windows-driver-content
description: The Begin method indicates that an operation is beginning. An estimate of the duration of the operation is provided when possible.
old-location: wmdm\iwmdmprogress_begin.htm
old-project: WMDM
ms.assetid: 207b7cb5-4471-4be9-8252-9d467d67d7a2
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: Begin, Begin method [windows Media Device Manager], Begin method [windows Media Device Manager],IWMDMProgress interface, IWMDMProgress interface [windows Media Device Manager],Begin method, IWMDMProgress.Begin, IWMDMProgress::Begin, IWMDMProgressBegin, mswmdm/IWMDMProgress::Begin, wmdm.iwmdmprogress_begin
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMProgress.Begin
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

