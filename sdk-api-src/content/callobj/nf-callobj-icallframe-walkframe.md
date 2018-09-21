---
UID: NF:callobj.ICallFrame.WalkFrame
title: ICallFrame::WalkFrame
author: windows-sdk-content
description: Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.
old-location: com\icallframe_walkframe.htm
tech.root: com
ms.assetid: 64e4967b-6b54-4416-ae10-04987f13d39a
ms.author: windowssdkdev
ms.date: 09/14/2018
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
 - ICallFrame.WalkFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICallFrame::WalkFrame


## -description


Searches for interface pointers that are reachable from [in], [in, out], or [out] parameters of the frame.


## -parameters




### -param walkWhat [in]

Flags from the <a href="https://msdn.microsoft.com/en-us/library/ms682455(v=VS.85).aspx">CALLFRAME_WALK</a> enumeration.


### -param pWalker [in]

A pointer to an instance of the <a href="https://msdn.microsoft.com/en-us/library/ms679746(v=VS.85).aspx">ICallFrameWalker</a> interface. When specified, a call back is made for each interface pointer encountered. This parameter is optional.


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




<a href="https://msdn.microsoft.com/en-us/library/ms683709(v=VS.85).aspx">ICallFrame</a>
 

 

