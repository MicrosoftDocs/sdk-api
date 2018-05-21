---
UID: NF:callobj.ICallFrame.WalkFrame
title: ICallFrame::WalkFrame
author: windows-driver-content
description: Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.
old-location: com\icallframe_walkframe.htm
old-project: com
ms.assetid: 64e4967b-6b54-4416-ae10-04987f13d39a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICallFrame interface [COM],WalkFrame method, ICallFrame.WalkFrame, ICallFrame::WalkFrame, WalkFrame, WalkFrame method [COM], WalkFrame method [COM],ICallFrame interface, _com_icallframe_walkframe, callobj/ICallFrame::WalkFrame, com.icallframe_walkframe
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
-	ICallFrame.WalkFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICallFrame::WalkFrame


## -description


Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.


## -parameters




### -param walkWhat [in]

Flags from the <a href="https://msdn.microsoft.com/52327707-43b0-4041-8fa1-62a9a62dc6b7">CALLFRAME_WALK</a> enumeration.


### -param pWalker [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/1eeb00a3-d3c5-46f0-95a8-f694f802894b">ICallFrameWalker</a> interface. When specified, a call back is made for each interface pointer encountered. This parameter is optional.


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
 

 

