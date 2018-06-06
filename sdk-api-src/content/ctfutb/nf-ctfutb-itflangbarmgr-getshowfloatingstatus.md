---
UID: NF:ctfutb.ITfLangBarMgr.GetShowFloatingStatus
title: ITfLangBarMgr::GetShowFloatingStatus
author: windows-sdk-content
description: ITfLangBarMgr::GetShowFloatingStatus method
old-location: tsf\itflangbarmgr_getshowfloatingstatus.htm
old-project: TSF
ms.assetid: ec187bf0-edf7-4d90-a102-92bb5b58ebdc
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetShowFloatingStatus, GetShowFloatingStatus method [Text Services Framework], GetShowFloatingStatus method [Text Services Framework],ITfLangBarMgr interface, ITfLangBarMgr interface [Text Services Framework],GetShowFloatingStatus method, ITfLangBarMgr.GetShowFloatingStatus, ITfLangBarMgr::GetShowFloatingStatus, _tsf_itflangbarmgr_getshowfloatingstatus_ref, ctfutb/ITfLangBarMgr::GetShowFloatingStatus, tsf.itflangbarmgr_getshowfloatingstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TfLBIClick
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfLangBarMgr.GetShowFloatingStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarMgr::GetShowFloatingStatus


## -description




## -parameters




### -param pdwFlags [out]

Indicates current language bar display settings. For a list of bitfield values, see <a href="https://msdn.microsoft.com/f49987c7-476d-4add-9d43-83de78693420">ITfLangBarMgr::ShowFloating</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/60bd765f-0846-47f5-af1b-bc8e72720841">ITfLangBarMgr</a>



<a href="https://msdn.microsoft.com/f49987c7-476d-4add-9d43-83de78693420">ITfLangBarMgr::ShowFloating
      </a>
 

 

