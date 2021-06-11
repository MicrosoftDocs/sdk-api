---
UID: NF:wpcapi.IWindowsParentalControlsCore.GetWebFilterInfo
title: IWindowsParentalControlsCore::GetWebFilterInfo (wpcapi.h)
description: Retrieves the name and identifier of the currently active Web Content Filter.
helpviewer_keywords: ["GetWebFilterInfo","GetWebFilterInfo method","GetWebFilterInfo method","IWindowsParentalControlsCore interface","IWindowsParentalControlsCore interface","GetWebFilterInfo method","IWindowsParentalControlsCore.GetWebFilterInfo","IWindowsParentalControlsCore::GetWebFilterInfo","parcon.iwindowsparentalcontrols_getwebfilterinfo","wpcapi/IWindowsParentalControlsCore::GetWebFilterInfo"]
old-location: parcon\iwindowsparentalcontrols_getwebfilterinfo.htm
tech.root: parcon
ms.assetid: 5073f335-fe55-43db-9186-aaa675384ea3
ms.date: 12/05/2018
ms.keywords: GetWebFilterInfo, GetWebFilterInfo method, GetWebFilterInfo method,IWindowsParentalControlsCore interface, IWindowsParentalControlsCore interface,GetWebFilterInfo method, IWindowsParentalControlsCore.GetWebFilterInfo, IWindowsParentalControlsCore::GetWebFilterInfo, parcon.iwindowsparentalcontrols_getwebfilterinfo, wpcapi/IWindowsParentalControlsCore::GetWebFilterInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsParentalControlsCore::GetWebFilterInfo
 - wpcapi/IWindowsParentalControlsCore::GetWebFilterInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWindowsParentalControlsCore.GetWebFilterInfo
---

# IWindowsParentalControlsCore::GetWebFilterInfo


## -description

Retrieves the name and identifier of the currently active Web Content Filter.

## -parameters

### -param pguidID [out]

The GUID of the currently active Web Content Filter.

### -param ppszName [in, out]

The name of the currently active Web Content Filter.

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

<a href="/windows/desktop/api/wpcapi/nn-wpcapi-iwindowsparentalcontrols">IWindowsParentalControls</a>



<a href="nn-wpcapi-iwindowsparentalcontrolscore.md">IWindowsParentalControlsCore</a>