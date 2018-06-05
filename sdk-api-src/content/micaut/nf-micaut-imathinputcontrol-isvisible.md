---
UID: NF:micaut.IMathInputControl.IsVisible
title: IMathInputControl::IsVisible
author: windows-sdk-content
description: Determines whether the control is visible.
old-location: tablet\imathinputcontrol_isvisible.htm
old-project: tablet
ms.assetid: 4efc0fd5-5f07-4664-8143-46a5695c04df
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IMathInputControl interface [Tablet PC],IsVisible method, IMathInputControl.IsVisible, IMathInputControl::IsVisible, IsVisible, IsVisible method [Tablet PC], IsVisible method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::IsVisible, tablet.imathinputcontrol_isvisible
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: micaut.h
req.include-header: Micaut.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Micaut.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	micaut.h
api_name:
-	IMathInputControl.IsVisible
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl::IsVisible


## -description


Determines whether the control is visible.


## -parameters




### -param pvbShown [out]

<b>VARIANT_TRUE</b> to show the control; <b>VARIANT_FALSE</b> to hide the control.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pvbShown</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

