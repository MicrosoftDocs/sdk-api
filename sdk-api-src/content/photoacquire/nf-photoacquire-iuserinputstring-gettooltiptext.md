---
UID: NF:photoacquire.IUserInputString.GetTooltipText
title: IUserInputString::GetTooltipText (photoacquire.h)
description: The GetTooltipText method retrieves the tooltip text displayed for a control.
helpviewer_keywords: ["GetTooltipText","GetTooltipText method [Picture Acquisition]","GetTooltipText method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetTooltipText method","IUserInputString.GetTooltipText","IUserInputString::GetTooltipText","IUserInputStringGetTooltipText","photoacquire/IUserInputString::GetTooltipText","picacq.iuserinputstring_gettooltiptext"]
old-location: picacq\iuserinputstring_gettooltiptext.htm
tech.root: picacq
ms.assetid: f57b247c-bd6d-46ea-be95-a239c1b087ce
ms.date: 12/05/2018
ms.keywords: GetTooltipText, GetTooltipText method [Picture Acquisition], GetTooltipText method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetTooltipText method, IUserInputString.GetTooltipText, IUserInputString::GetTooltipText, IUserInputStringGetTooltipText, photoacquire/IUserInputString::GetTooltipText, picacq.iuserinputstring_gettooltiptext
req.header: photoacquire.h
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserInputString::GetTooltipText
 - photoacquire/IUserInputString::GetTooltipText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IUserInputString.GetTooltipText
---

# IUserInputString::GetTooltipText


## -description

The <code>GetTooltipText</code> method retrieves the tooltip text displayed for a control.

## -parameters

### -param pbstrTooltipText [out]

Pointer to a string containing the tooltip text.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>