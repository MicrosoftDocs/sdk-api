---
UID: NF:photoacquire.IUserInputString.GetStringType
title: IUserInputString::GetStringType (photoacquire.h)
description: The GetStringType method retrieves a value indicating the type of string to obtain from the user.
helpviewer_keywords: ["GetStringType","GetStringType method [Picture Acquisition]","GetStringType method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetStringType method","IUserInputString.GetStringType","IUserInputString::GetStringType","IUserInputStringGetStringType","photoacquire/IUserInputString::GetStringType","picacq.iuserinputstring_getstringtype"]
old-location: picacq\iuserinputstring_getstringtype.htm
tech.root: picacq
ms.assetid: 57f0c750-9c66-4c30-adc1-0cfd23d878d1
ms.date: 12/05/2018
ms.keywords: GetStringType, GetStringType method [Picture Acquisition], GetStringType method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetStringType method, IUserInputString.GetStringType, IUserInputString::GetStringType, IUserInputStringGetStringType, photoacquire/IUserInputString::GetStringType, picacq.iuserinputstring_getstringtype
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
 - IUserInputString::GetStringType
 - photoacquire/IUserInputString::GetStringType
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
 - IUserInputString.GetStringType
---

# IUserInputString::GetStringType


## -description

The <code>GetStringType</code> method retrieves a value indicating the type of string to obtain from the user.

## -parameters

### -param pnStringType [out]

Pointer to an integer value containing the string type.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td><b>USER_INPUT_DEFAULT</b></td>
<td>Specifies that any string is allowed.</td>
</tr>
<tr>
<td><b>USER_INPUT_PATH_ELEMENT</b></td>
<td>Specifies that the string will not accept characters that are illegal in file or directory names (such as * or /).</td>
</tr>
</table>

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



<a href="/windows/desktop/api/photoacquire/ne-photoacquire-user_input_string_type">USER_INPUT_STRING_TYPE</a>