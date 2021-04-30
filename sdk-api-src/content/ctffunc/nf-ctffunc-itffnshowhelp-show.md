---
UID: NF:ctffunc.ITfFnShowHelp.Show
title: ITfFnShowHelp::Show (ctffunc.h)
description: ITfFnShowHelp::Show method
helpviewer_keywords: ["ITfFnShowHelp interface [Text Services Framework]","Show method","ITfFnShowHelp.Show","ITfFnShowHelp::Show","Show","Show method [Text Services Framework]","Show method [Text Services Framework]","ITfFnShowHelp interface","_tsf_itffnshowhelp_show_ref","ctffunc/ITfFnShowHelp::Show","tsf.itffnshowhelp_show"]
old-location: tsf\itffnshowhelp_show.htm
tech.root: TSF
ms.assetid: e150dffe-4a02-4d16-9017-f86111970aea
ms.date: 12/05/2018
ms.keywords: ITfFnShowHelp interface [Text Services Framework],Show method, ITfFnShowHelp.Show, ITfFnShowHelp::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfFnShowHelp interface, _tsf_itffnshowhelp_show_ref, ctffunc/ITfFnShowHelp::Show, tsf.itffnshowhelp_show
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnShowHelp::Show
 - ctffunc/ITfFnShowHelp::Show
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnShowHelp.Show
---

# ITfFnShowHelp::Show


## -description

Called when the user selects a text service help menu item.

## -parameters

### -param hwndParent [in]

Handle of the parent window. This value can be <b>NULL</b>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

The text service should not wait for the help UI to be complete before returning from this method.

