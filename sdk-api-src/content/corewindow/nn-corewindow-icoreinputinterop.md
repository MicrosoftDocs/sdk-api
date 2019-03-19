---
UID: NN:corewindow.ICoreInputInterop
title: ICoreInputInterop (corewindow.h)
author: windows-sdk-content
description: Enables an input source on a Windows Store app's CoreInput object.
old-location: winrt\icoreinputinterop.htm
tech.root: WinRT
ms.assetid: F7BA7EFB-D9DC-4FF2-97A4-C4818BCBD599
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICoreInputInterop, ICoreInputInterop interface [Windows Runtime], ICoreInputInterop interface [Windows Runtime],described, corewindow/ICoreInputInterop, winrt.icoreinputinterop
ms.topic: interface
req.header: corewindow.h
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
 - corewindow.h
api_name:
 - ICoreInputInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICoreInputInterop interface


## -description


Enables an input source on a Windows Store app's <a href="w_ui_core.coreinput">CoreInput</a> object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreInputInterop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICoreInputInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICoreInputInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/693180F5-2C19-47CD-9514-F0CEA1849A4A">SetInputSource</a>
</td>
<td align="left" width="63%">
Sets the input source for an app's <a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a> or <a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreInputInterop</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/94575082-014D-42E3-8191-F79912CBDB2A">MessageHandled</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Sets whether or not the message to the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> has been handled.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a> or <a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a> object defines the basic keyboard and pointer input events  for a Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/3075a07b-c432-482e-a44b-494014ff13fc">CoreComponentInputSource</a>



<a href="https://msdn.microsoft.com/917cbf9f-bd19-4e05-bcd1-cf6a86f16e65">CoreIndependentInputSource</a>



<a href="w_ui_core.coreinput">CoreInput</a>
 

 

