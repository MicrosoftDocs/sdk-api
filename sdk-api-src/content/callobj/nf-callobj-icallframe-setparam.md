---
UID: NF:callobj.ICallFrame.SetParam
title: ICallFrame::SetParam (callobj.h)
description: Sets the value of a specified parameter in the call frame.
old-location: com\icallframe_setparam.htm
tech.root: com
ms.assetid: ec828206-d49f-49da-91fc-554d703b53db
ms.date: 12/05/2018
ms.keywords: ICallFrame interface [COM],SetParam method, ICallFrame.SetParam, ICallFrame::SetParam, SetParam, SetParam method [COM], SetParam method [COM],ICallFrame interface, _com_icallframe_setparam, callobj/ICallFrame::SetParam, com.icallframe_setparam
f1_keywords:
- callobj/ICallFrame.SetParam
dev_langs:
- c++
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
- Callobj.h
api_name:
- ICallFrame.SetParam
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICallFrame::SetParam


## -description


Sets the value of a specified parameter in the call frame.


## -parameters




### -param iparam [in]

The parameter number.


### -param pvar [in]

The new value for the parameter.


## -returns



This method can return the following values.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>
 

 

