---
UID: NF:wmp.IWMPError.get_errorCount
title: IWMPError::get_errorCount (wmp.h)
description: The get_errorCount method retrieves the number of errors in the error queue.
helpviewer_keywords: ["IWMPError interface [Windows Media Player]","get_errorCount method","IWMPError.get_errorCount","IWMPError::get_errorCount","IWMPErrorget_errorCount","get_errorCount","get_errorCount method [Windows Media Player]","get_errorCount method [Windows Media Player]","IWMPError interface","wmp.iwmperror_get_errorcount","wmp/IWMPError::get_errorCount"]
old-location: wmp\iwmperror_get_errorcount.htm
tech.root: WMP
ms.assetid: 0ad21e08-4566-4f3a-8506-308432996481
ms.date: 12/05/2018
ms.keywords: IWMPError interface [Windows Media Player],get_errorCount method, IWMPError.get_errorCount, IWMPError::get_errorCount, IWMPErrorget_errorCount, get_errorCount, get_errorCount method [Windows Media Player], get_errorCount method [Windows Media Player],IWMPError interface, wmp.iwmperror_get_errorcount, wmp/IWMPError::get_errorCount
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPError::get_errorCount
 - wmp/IWMPError::get_errorCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPError.get_errorCount
---

# IWMPError::get_errorCount


## -description

The <b>get_errorCount</b> method retrieves the number of errors in the error queue.

## -parameters

### -param plNumErrors [out]

Pointer to a <b>long</b> containing the number of errors.

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
</table>

## -remarks

You should set a <b>VARIANT_BOOL</b> to <b>FALSE</b> and pass it into <b>IWMPSettings::put_enableErrorDialogs</b> if you choose to display custom error messages.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>