---
UID: NN:shldisp.IShellDispatch6
title: IShellDispatch6
author: windows-sdk-content
description: Extends the IShellDispatch5 object.
old-location: shell\IShellDispatch6.htm
old-project: shell
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IShellDispatch6, IShellDispatch6 object [Windows Shell], IShellDispatch6 object [Windows Shell],described, shell.IShellDispatch6, shldisp/IShellDispatch6
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDispatch6
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellDispatch6 interface


## -description


Extends the <a href="https://msdn.microsoft.com/9170340a-0f11-4ec9-877d-fb7fef9888b2">IShellDispatch5</a> object. In addition to the properties and methods supported by <b>IShellDispatch5</b>, <b>IShellDispatch6</b> adds a method that displays the Apps Search pane.

            
<div class="alert"><b>Note</b>  <b>IShellDispatch6</b> is implemented and accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270130">Shell</a> object.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch6</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellDispatch6</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B5861125-2B21-4C47-8425-026381B2F677">SearchCommand</a>
</td>
<td align="left" width="63%">
Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.

</td>
</tr>
</table> 


## -see-also




<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a>



<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>



<a href="https://msdn.microsoft.com/74687929-0777-479b-9853-2b0cf4b6adc9">IShellDispatch2</a>



<a href="https://msdn.microsoft.com/89d0aa4d-844d-497d-82bb-bcc2bcf9c78b">IShellDispatch3</a>



<a href="https://msdn.microsoft.com/4fe37e38-ee71-41f0-b620-35fdc18f9dbb">IShellDispatch4</a>



<a href="https://msdn.microsoft.com/9170340a-0f11-4ec9-877d-fb7fef9888b2">IShellDispatch5</a>



<a href="https://msdn.microsoft.com/75fc151e-5b9e-476b-b4e5-b848917357a8">Shell Object</a>
 

 

