---
UID: NF:callobj.ICallFrame.FreeParam
title: ICallFrame::FreeParam
author: windows-sdk-content
description: Frees the specified parameter in the frame.
old-location: com\icallframe_freeparam.htm
tech.root: com
ms.assetid: b141bfc4-de1b-4251-b88f-551d0805e9b6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FreeParam, FreeParam method [COM], FreeParam method [COM],ICallFrame interface, ICallFrame interface [COM],FreeParam method, ICallFrame.FreeParam, ICallFrame::FreeParam, _com_icallframe_freeparam, callobj/ICallFrame::FreeParam, com.icallframe_freeparam
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICallFrame.FreeParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- callobj.h
: 
- ICallFrame.FreeParam
: 
---

# ICallFrame::FreeParam


## -description


Frees the specified parameter in the frame.


## -parameters




### -param iparam [in]

The number of the parameter to be freed.


### -param freeFlags [in]

Represents flags from the <a href="https://msdn.microsoft.com/6a048133-7a89-4b55-afd3-5eb722d41914">CALLFRAME_FREE</a> enumeration.


### -param pWalkerFree [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. When specified, a callback is made for each interface pointer encountered while freeing occurs. If this parameter is not specified, then the interface pointers are freed by the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


### -param nullFlags [in]

Represents flags from the <a href="https://msdn.microsoft.com/99d83bdc-a33b-4233-84c6-350274f42965">CALLFRAME_NULL</a> enumeration.


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




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

