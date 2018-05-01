---
UID: NN:wia_lh.IWiaLog
title: IWiaLog
author: windows-driver-content
description: The IWiaLog interface provides methods to enable minidrivers to log trace, error, and warning messages to the diagnostic log file Wiaservc.log.
old-location: image\iwialog_interface.htm
old-project: image
ms.assetid: b56cb3f0-1053-4104-b223-e7448a832f33
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaLog, IWiaLog interface [Imaging Devices], IWiaLog interface [Imaging Devices], described, IWiaLog_0284e394-6bc5-40b8-8174-0041bfc0d5dd.xml, image.iwialog_interface, wia_lh/IWiaLog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_lh.h
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wia_lh.h
api_name:
-	IWiaLog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaLog interface


## -description


<div class="alert"><b>Note</b>  <p class="note">The IWiaLog interface is obsolete for Microsoft Windows XP and later and is no longer supported. Instead, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540599">Diagnostic Log Macros</a>.

</div><div> </div>
The <b>IWiaLog</b> interface provides methods to enable minidrivers to log trace, error, and warning messages to the diagnostic log file Wiaservc.log. The prototypes for the methods appear in Wia.h. The diagnostic log file Wiaservc.log is found in the Windows directory, or in the directory returned by the GetWindowsDirectory system API call, which is described in the Microsoft Windows SDK documentation.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaLog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaLog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaLog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d9b770-c2b6-483d-a6d7-070ac2a55133">hResult</a>
</td>
<td align="left" width="63%">
Note that the <b>IWiaLog</b> interface is <b>obsolete </b>for Microsoft Windows XP and later, and is no longer supported. Instead, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540599">Diagnostic Log Macros</a>.

The <b>IWiaLog::hResult</b> method translates an HRESULT value into a string and writes the string to <i>Wiaservc.log</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef637329-a291-445b-8ac7-6e55d5d7931e">InitializeLog</a>
</td>
<td align="left" width="63%">
Note that the <b>IWiaLog</b> interface is <b>obsolete</b> for Microsoft Windows XP and later, and is no longer supported. Instead, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540599">Diagnostic Log Macros</a>.

The <b>IWiaLog::InitializeLog</b> method initializes the <b>lWiaLog</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406307">Log</a>
</td>
<td align="left" width="63%">
The <b>IWiaLog</b> interface is obsolete for Windows XP and later, and is no longer supported. Use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540599">Diagnostic Log Macros</a> instead.The <b>IWiaLog::Log</b> method writes a diagnostic log message to <i>Wiaservc.log</i>.

</td>
</tr>
</table> 

