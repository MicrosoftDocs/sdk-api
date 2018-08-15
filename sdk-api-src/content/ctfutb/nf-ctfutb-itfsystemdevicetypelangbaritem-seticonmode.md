---
UID: NF:ctfutb.ITfSystemDeviceTypeLangBarItem.SetIconMode
title: ITfSystemDeviceTypeLangBarItem::SetIconMode
author: windows-sdk-content
description: ITfSystemDeviceTypeLangBarItem::SetIconMode method
old-location: tsf\itfsystemdevicetypelangbaritem_seticonmode.htm
old-project: TSF
ms.assetid: 25124539-4bf9-4299-b441-9a5fac18b60d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],SetIconMode method, ITfSystemDeviceTypeLangBarItem.SetIconMode, ITfSystemDeviceTypeLangBarItem::SetIconMode, SetIconMode, SetIconMode method [Text Services Framework], SetIconMode method [Text Services Framework],ITfSystemDeviceTypeLangBarItem interface, TF_DTLBI_USEPROFILEICON, _tsf_itfsystemdevicetypelangbaritem_seticonmode_ref, ctfutb/ITfSystemDeviceTypeLangBarItem::SetIconMode, tsf.itfsystemdevicetypelangbaritem_seticonmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
 - msctf.dll
api_name:
 - ITfSystemDeviceTypeLangBarItem.SetIconMode
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemDeviceTypeLangBarItem::SetIconMode


## -description




## -parameters




### -param dwFlags [in]

Specifies how the system language bar item should display the icon. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The system language bar item should display a default icon for the item.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_DTLBI_USEPROFILEICON"></a><a id="tf_dtlbi_useprofileicon"></a><dl>
<dt><b>TF_DTLBI_USEPROFILEICON</b></dt>
</dl>
</td>
<td width="60%">
The system language bar item should display the icon specified for the language profile.

</td>
</tr>
</table>
 


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
The system language bar item does not support this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0dc32f10-eecd-4203-992c-80eb0f991615">ITfSystemDeviceTypeLangBarItem</a>



<a href="https://msdn.microsoft.com/c1740636-7ba3-4748-9005-ee94d04dbb15">Miscellaneous Language Bar Constants</a>
 

 

