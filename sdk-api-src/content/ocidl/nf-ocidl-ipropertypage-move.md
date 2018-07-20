---
UID: NF:ocidl.IPropertyPage.Move
title: IPropertyPage::Move
author: windows-sdk-content
description: Positions and resizes the property page dialog box within the frame.
old-location: com\ipropertypage_move.htm
old-project: com
ms.assetid: 305857c2-cb3a-4a56-9db3-b986b278bd02
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IPropertyPage interface [COM],Move method, IPropertyPage.Move, IPropertyPage::Move, Move, Move method [COM], Move method [COM],IPropertyPage interface, _ctrl_ipropertypage_move, com.ipropertypage_move, ocidl/IPropertyPage::Move
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPage.Move
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyPage::Move


## -description


Positions and resizes the property page dialog box within the frame.


## -parameters




### -param pRect [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure containing the positioning information for the property page dialog box.


## -returns



This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>prc</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The rectangle specified by <i>prc</i> is treated identically to that passed to <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="https://msdn.microsoft.com/4756d06d-0ffc-4214-9c2b-d9cb169b4337">IPropertyPage::Activate</a> and before a corresponding call to <a href="https://msdn.microsoft.com/545f7c3d-3c6f-42c2-b472-3da3bc184200">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The page must create its dialog box with the placement and dimensions described by this structure.




## -see-also




<a href="https://msdn.microsoft.com/ad2cb3ae-dd24-4774-95bd-f5a0773c68b1">IPropertyPage</a>
 

 

