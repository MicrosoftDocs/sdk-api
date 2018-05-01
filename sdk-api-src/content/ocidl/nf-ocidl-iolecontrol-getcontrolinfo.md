---
UID: NF:ocidl.IOleControl.GetControlInfo
title: IOleControl::GetControlInfo method
author: windows-driver-content
description: Retrieves information about the control's keyboard mnemonics and behavior.
old-location: com\iolecontrol_getcontrolinfo.htm
old-project: com
ms.assetid: defb7509-e586-45a0-9e56-de9eba17f18e
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetControlInfo method [COM], GetControlInfo method [COM], IOleControl interface, GetControlInfo,IOleControl.GetControlInfo, IOleControl, IOleControl interface [COM], GetControlInfo method, IOleControl::GetControlInfo, _ctrl_iolecontrol_getcontrolinfo, com.iolecontrol_getcontrolinfo, ocidl/IOleControl::GetControlInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IOleControl.GetControlInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOleControl::GetControlInfo method


## -description


Retrieves information about the control's keyboard mnemonics and behavior.


## -parameters




### -param pCI [in, out]

A pointer to a <a href="https://msdn.microsoft.com/3f22dc1d-554a-4dd1-a79a-121117f65caf">CONTROLINFO</a> structure that receives the information.


## -returns



This method can return the standard return value E_OUTOFMEMORY, as well as the following values.

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
The method completed succesfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The control has no mnemonics.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pCI</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ef85dce6-b680-4a72-9277-4cfdab27cbbc">IOleControl</a>
 

 

