---
UID: NF:ctffunc.ITfFnConfigureRegisterEudc.Show
title: ITfFnConfigureRegisterEudc::Show (ctffunc.h)
description: The ITfFnConfigureRegisterEudc::Show method shows the EUDC key sequence register UI.
helpviewer_keywords: ["ITfFnConfigureRegisterEudc interface [Text Services Framework]","Show method","ITfFnConfigureRegisterEudc.Show","ITfFnConfigureRegisterEudc::Show","Show","Show method [Text Services Framework]","Show method [Text Services Framework]","ITfFnConfigureRegisterEudc interface","ctffunc/ITfFnConfigureRegisterEudc::Show","tsf.itffnconfigureregistereudc_show"]
old-location: tsf\itffnconfigureregistereudc_show.htm
tech.root: TSF
ms.assetid: 40279381-7c1c-4b11-92c9-200b763e7c7d
ms.date: 12/05/2018
ms.keywords: ITfFnConfigureRegisterEudc interface [Text Services Framework],Show method, ITfFnConfigureRegisterEudc.Show, ITfFnConfigureRegisterEudc::Show, Show, Show method [Text Services Framework], Show method [Text Services Framework],ITfFnConfigureRegisterEudc interface, ctffunc/ITfFnConfigureRegisterEudc::Show, tsf.itffnconfigureregistereudc_show
req.header: ctffunc.h
req.include-header: Msctf.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfFnConfigureRegisterEudc::Show
 - ctffunc/ITfFnConfigureRegisterEudc::Show
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
 - ITfFnConfigureRegisterEudc.Show
---

# ITfFnConfigureRegisterEudc::Show


## -description

The ITfFnConfigureRegisterEudc::Show method shows the EUDC key sequence register UI.

## -parameters

### -param hwndParent [in]

[in] Handle of the parent window. The text service typically uses this as the parent or owner window when creating a dialog box.

### -param langid [in]

[in] Contains a LANGID value that specifies the identifier of the language.

### -param rguidProfile [in]

[in] Contains a GUID value that specifies the language profile identifier that the text service is under.

### -param bstrRegistered

[in, unique] Contains a BSTR that contains the EUDC to be registered with the text service. This is optional and can be <b>NULL</b>. If <b>NULL</b>, the text service should display a default register EUDC dialog box.

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

