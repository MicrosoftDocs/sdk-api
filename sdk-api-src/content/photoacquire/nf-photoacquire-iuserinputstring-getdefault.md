---
UID: NF:photoacquire.IUserInputString.GetDefault
title: IUserInputString::GetDefault (photoacquire.h)
description: The GetDefault method retrieves the default string used to initialize an edit control (or equivalent).
old-location: picacq\iuserinputstring_getdefault.htm
tech.root: acquisition
ms.assetid: d9e967f9-47ed-4b55-a728-fe6432b44efd
ms.date: 12/05/2018
ms.keywords: GetDefault, GetDefault method [Picture Acquisition], GetDefault method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetDefault method, IUserInputString.GetDefault, IUserInputString::GetDefault, IUserInputStringGetDefault, photoacquire/IUserInputString::GetDefault, picacq.iuserinputstring_getdefault
f1_keywords:
- photoacquire/IUserInputString.GetDefault
dev_langs:
- c++
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
- IUserInputString.GetDefault
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUserInputString::GetDefault


## -description



The <code>GetDefault</code> method retrieves the default string used to initialize an edit control (or equivalent).




## -parameters




### -param pbstrDefault [out]

Pointer to a string containing the default value used to initialize the edit control.


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
The pointer passed was <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>
 

 

