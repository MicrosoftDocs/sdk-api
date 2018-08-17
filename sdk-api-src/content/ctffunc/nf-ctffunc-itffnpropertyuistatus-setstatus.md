---
UID: NF:ctffunc.ITfFnPropertyUIStatus.SetStatus
title: ITfFnPropertyUIStatus::SetStatus
author: windows-sdk-content
description: ITfFnPropertyUIStatus::SetStatus method
old-location: tsf\itffnpropertyuistatus_setstatus.htm
old-project: TSF
ms.assetid: 817329fb-521a-426a-88d8-b36ee161b6b9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnPropertyUIStatus interface [Text Services Framework],SetStatus method, ITfFnPropertyUIStatus.SetStatus, ITfFnPropertyUIStatus::SetStatus, SetStatus, SetStatus method [Text Services Framework], SetStatus method [Text Services Framework],ITfFnPropertyUIStatus interface, _tsf_itffnpropertyuistatus_setstatus_ref, ctffunc/ITfFnPropertyUIStatus::SetStatus, tsf.itffnpropertyuistatus_setstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnPropertyUIStatus.SetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnPropertyUIStatus::SetStatus


## -description




## -parameters




### -param refguidProp [in]

Specifies the property identifier. This can be a custom identifier or one of the <a href="https://msdn.microsoft.com/en-us/library/ms629017(v=VS.85).aspx">predefined property</a> identifiers.


### -param dw [in]

Contains the new property UI status. See the <i>pdw</i> parameter of <a href="https://msdn.microsoft.com/en-us/library/ms538965(v=VS.85).aspx">ITfFnPropertyUIStatus::GetStatus</a> for possible values.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The text service does not support this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538963(v=VS.85).aspx">ITfFnPropertyUIStatus</a>



<a href="https://msdn.microsoft.com/aef8c1b4-3cda-4fa3-ae8c-a8f8da4840b5">ITfFnPropertyUIStatus::GetStatus
      </a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">Predefined Properties
      </a>
 

 

