---
UID: NF:micaut.IMathInputControl.SetPosition
title: IMathInputControl::SetPosition (micaut.h)
description: Modifies the location and size of the control.
helpviewer_keywords: ["IMathInputControl interface [Tablet PC]","SetPosition method","IMathInputControl.SetPosition","IMathInputControl::SetPosition","SetPosition","SetPosition method [Tablet PC]","SetPosition method [Tablet PC]","IMathInputControl interface","micaut/IMathInputControl::SetPosition","tablet.imathinputcontrol_setposition"]
old-location: tablet\imathinputcontrol_setposition.htm
tech.root: tablet
ms.assetid: 9b5fc988-7c93-47d4-8661-4cef56cab0d0
ms.date: 12/05/2018
ms.keywords: IMathInputControl interface [Tablet PC],SetPosition method, IMathInputControl.SetPosition, IMathInputControl::SetPosition, SetPosition, SetPosition method [Tablet PC], SetPosition method [Tablet PC],IMathInputControl interface, micaut/IMathInputControl::SetPosition, tablet.imathinputcontrol_setposition
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMathInputControl::SetPosition
 - micaut/IMathInputControl::SetPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl.SetPosition
---

# IMathInputControl::SetPosition


## -description

Modifies the location and size of the control.

## -parameters

### -param Left [in]

The leftmost position of the control.

### -param Top [in]

The highest position of the control.

### -param Right [in]

The rightmost position of the control.

### -param Bottom [in]

The lowest position of the control.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The control was resized but the resulting width, height, or both are not equal to the input parameters.

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
</table>

## -remarks

This method can be called regardless of the control visibility state.

This method will succeed even if parameters are not valid. If the rectangle is larger than the maximum allowed size of the control (desktop window), the maximum possible size is used instead. If the rectangle is smaller than the minimal size of the control, or too small to keep the ink and result preview intact, the minimal possible size is used instead.


If  the method returns <b>S_FALSE</b>, the  <a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getposition">GetPosition</a> method will return the actual size characteristics of the control.

## -see-also

<a href="/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getposition">GetPosition</a>



<a href="/windows/desktop/api/micaut/nn-micaut-imathinputcontrol">IMathInputControl</a>