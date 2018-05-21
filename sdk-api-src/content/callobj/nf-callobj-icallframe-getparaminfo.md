---
UID: NF:callobj.ICallFrame.GetParamInfo
title: ICallFrame::GetParamInfo
author: windows-driver-content
description: Retrieves the information for the specified parameter.
old-location: com\icallframe_getparaminfo.htm
old-project: com
ms.assetid: fb75930d-8e1b-4e97-87f2-bb9d171658a8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetParamInfo, GetParamInfo method [COM], GetParamInfo method [COM],ICallFrame interface, ICallFrame interface [COM],GetParamInfo method, ICallFrame.GetParamInfo, ICallFrame::GetParamInfo, _com_icallframe_getparaminfo, callobj/ICallFrame::GetParamInfo, com.icallframe_getparaminfo
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
req.typenames: CALLFRAME_COPY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Callobj.h
api_name:
-	ICallFrame.GetParamInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::GetParamInfo


## -description


Retrieves the information for the specified parameter.


## -parameters




### -param iparam [in]

The parameter number.


### -param pInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/0f3a1e81-c8b6-4141-8712-c600b30a2779">CALLFRAMEPARAMINFO</a> structure.


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
 

 

