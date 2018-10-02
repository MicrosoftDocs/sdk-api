---
UID: NF:ocidl.IPropertyPage.TranslateAccelerator
title: IPropertyPage::TranslateAccelerator
author: windows-sdk-content
description: Passes a keystroke to the property page for processing.
old-location: com\ipropertypage_translateaccelerator.htm
tech.root: com
ms.assetid: 70501c3d-257c-4981-b841-4bd45f0bec27
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IPropertyPage interface [COM],TranslateAccelerator method, IPropertyPage.TranslateAccelerator, IPropertyPage::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IPropertyPage interface, _ctrl_ipropertypage_translateaccelerator, com.ipropertypage_translateaccelerator, ocidl/IPropertyPage::TranslateAccelerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IPropertyPage.TranslateAccelerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyPage::TranslateAccelerator


## -description


Passes a keystroke to the property page for processing.


## -parameters




### -param pMsg [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a> structure describing the keystroke to be processed.


## -returns



This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
The property page handles the accelerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property page handles accelerators, but this one was not useful to it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The property page does not handle accelerators.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pMsg</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a> and before the corresponding call to <a href="https://msdn.microsoft.com/545f7c3d-3c6f-42c2-b472-3da3bc184200">IPropertyPage::Deactivate</a>.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

