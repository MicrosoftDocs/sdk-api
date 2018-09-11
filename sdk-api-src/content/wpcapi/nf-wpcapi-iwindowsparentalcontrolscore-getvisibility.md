---
UID: NF:wpcapi.IWindowsParentalControlsCore.GetVisibility
title: IWindowsParentalControlsCore::GetVisibility
author: windows-sdk-content
description: Indicates the visibility of the Parental Controls user interface.
old-location: parcon\iwindowsparentalcontrols_getvisibility.htm
tech.root: parcon
ms.assetid: 08217ad2-3b1e-4733-8ca2-4463ffe96516
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetVisibility, GetVisibility method, GetVisibility method,IWindowsParentalControlsCore interface, IWindowsParentalControlsCore interface,GetVisibility method, IWindowsParentalControlsCore.GetVisibility, IWindowsParentalControlsCore::GetVisibility, WPCFLAG_WPC_HIDDEN, WPCFLAG_WPC_VISIBLE, parcon.iwindowsparentalcontrols_getvisibility, wpcapi/IWindowsParentalControlsCore::GetVisibility
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - Wpcapi.h
api_name:
 - IWindowsParentalControlsCore.GetVisibility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsParentalControlsCore::GetVisibility


## -description


Indicates the visibility of the Parental Controls user interface.


## -parameters




### -param peVisibility [out]

Indicates whether the user interface is hidden. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WPC_VISIBLE"></a><a id="wpcflag_wpc_visible"></a><dl>
<dt><b>WPCFLAG_WPC_VISIBLE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The user interface is visible.

</td>
</tr>
<tr>
<td width="40%"><a id="WPCFLAG_WPC_HIDDEN"></a><a id="wpcflag_wpc_hidden"></a><dl>
<dt><b>WPCFLAG_WPC_HIDDEN</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The user interface is hidden.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f825388f-c4de-4bf2-8076-6efd81b6e030">IWindowsParentalControls</a>



<a href="https://msdn.microsoft.com/49F43A0F-5C93-4FEC-870B-17535DE674C5">IWindowsParentalControlsCore</a>
 

 

