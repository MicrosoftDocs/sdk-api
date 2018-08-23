---
UID: NF:callobj.ICallFrame.GetIIDAndMethod
title: ICallFrame::GetIIDAndMethod
author: windows-sdk-content
description: Retrieves the interface ID or the method number.
old-location: com\icallframe_getiidandmethod.htm
old-project: com
ms.assetid: 938798ef-ddc8-4182-9216-d130c4f0e4ae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetIIDAndMethod, GetIIDAndMethod method [COM], GetIIDAndMethod method [COM],ICallFrame interface, ICallFrame interface [COM],GetIIDAndMethod method, ICallFrame.GetIIDAndMethod, ICallFrame::GetIIDAndMethod, _com_icallframe_getiidandmethod, callobj/ICallFrame::GetIIDAndMethod, com.icallframe_getiidandmethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: callobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CALLFRAME_COPY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame.GetIIDAndMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::GetIIDAndMethod


## -description


Retrieves the interface ID or the method number.


## -parameters




### -param pIID [out]

A pointer to the interface ID.


### -param piMethod [out]

A pointer to the method number.


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
 

 

