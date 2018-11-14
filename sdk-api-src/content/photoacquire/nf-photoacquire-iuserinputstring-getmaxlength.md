---
UID: NF:photoacquire.IUserInputString.GetMaxLength
title: IUserInputString::GetMaxLength
author: windows-sdk-content
description: The GetMaxLength method retrieves the maximum string length the user interface (UI) should allow.
old-location: picacq\iuserinputstring_getmaxlength.htm
tech.root: acquisition
ms.assetid: 474b32f5-e8b3-49d2-a2de-a78244b9066e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMaxLength, GetMaxLength method [Picture Acquisition], GetMaxLength method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetMaxLength method, IUserInputString.GetMaxLength, IUserInputString::GetMaxLength, IUserInputStringGetMaxLength, photoacquire/IUserInputString::GetMaxLength, picacq.iuserinputstring_getmaxlength
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
 - IUserInputString.GetMaxLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- photoacquire.h
: 
- IUserInputString.GetMaxLength
: 
---

# IUserInputString::GetMaxLength


## -description



The <code>GetMaxLength</code> method retrieves the maximum string length the user interface (UI) should allow.




## -parameters




### -param pcchMaxLength [out]

Pointer to the size of the maximum string length in characters.


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
 

 

