---
UID: NF:photoacquire.IUserInputString.GetStringType
title: IUserInputString::GetStringType
author: windows-sdk-content
description: The GetStringType method retrieves a value indicating the type of string to obtain from the user.
old-location: picacq\iuserinputstring_getstringtype.htm
tech.root: acquisition
ms.assetid: 57f0c750-9c66-4c30-adc1-0cfd23d878d1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetStringType, GetStringType method [Picture Acquisition], GetStringType method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetStringType method, IUserInputString.GetStringType, IUserInputString::GetStringType, IUserInputStringGetStringType, photoacquire/IUserInputString::GetStringType, picacq.iuserinputstring_getstringtype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/f942fefc-2db1-4067-8311-f9ebbaca9d31">IUserInputString Interface</a>



<a href="https://msdn.microsoft.com/ac05f51e-4762-4360-9c38-7baf84eeb1e9">USER_INPUT_STRING_TYPE</a>
 

 

