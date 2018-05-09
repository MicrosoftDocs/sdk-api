---
UID: NF:msctf.ITfDisplayAttributeInfo.SetAttributeInfo
title: ITfDisplayAttributeInfo::SetAttributeInfo
author: windows-driver-content
description: ITfDisplayAttributeInfo::SetAttributeInfo method
old-location: tsf\itfdisplayattributeinfo_setattributeinfo.htm
old-project: TSF
ms.assetid: 3e9a472c-7992-48fc-be47-993f6d53f043
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ITfDisplayAttributeInfo interface [Text Services Framework],SetAttributeInfo method, ITfDisplayAttributeInfo.SetAttributeInfo, ITfDisplayAttributeInfo::SetAttributeInfo, SetAttributeInfo, SetAttributeInfo method [Text Services Framework], SetAttributeInfo method [Text Services Framework],ITfDisplayAttributeInfo interface, _tsf_itfdisplayattributeinfo_setattributeinfo_ref, msctf/ITfDisplayAttributeInfo::SetAttributeInfo, tsf.itfdisplayattributeinfo_setattributeinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfDisplayAttributeInfo.SetAttributeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDisplayAttributeInfo::SetAttributeInfo


## -description




## -parameters




### -param pda [in]

Pointer to a <a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE</a> structure that contains the new display attribute data.


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
The display attribute provider does not support attribute modification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pda</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



The implementation of this method should not call <a href="https://msdn.microsoft.com/0f906a19-16b8-47c1-adca-10d6da0cc7dd">ITfDisplayAttributeMgr::OnUpdateInfo</a> in response to this method. The caller must do so. This avoids redundant notifications if more than one attribute is modified. The caller must eventually call <b>ITfDisplayAttributeMgr::OnUpdateInfo</b> so that other clients will receive an attribute update notification.




## -see-also




<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a>



<a href="https://msdn.microsoft.com/0f906a19-16b8-47c1-adca-10d6da0cc7dd">
        ITfDisplayAttributeMgr::OnUpdateInfo
      </a>



<a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE
      </a>
 

 

