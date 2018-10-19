---
UID: NF:ctfutb.ITfSystemDeviceTypeLangBarItem.GetIconMode
title: ITfSystemDeviceTypeLangBarItem::GetIconMode
author: windows-sdk-content
description: ITfSystemDeviceTypeLangBarItem::GetIconMode method
old-location: tsf\itfsystemdevicetypelangbaritem_geticonmode.htm
tech.root: TSF
ms.assetid: 0ac293de-0a35-4b3a-98af-f47849fd7149
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetIconMode, GetIconMode method [Text Services Framework], GetIconMode method [Text Services Framework],ITfSystemDeviceTypeLangBarItem interface, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],GetIconMode method, ITfSystemDeviceTypeLangBarItem.GetIconMode, ITfSystemDeviceTypeLangBarItem::GetIconMode, _tsf_itfsystemdevicetypelangbaritem_geticonmode_ref, ctfutb/ITfSystemDeviceTypeLangBarItem::GetIconMode, tsf.itfsystemdevicetypelangbaritem_geticonmode
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSystemDeviceTypeLangBarItem.GetIconMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfSystemDeviceTypeLangBarItem::GetIconMode


## -description




## -parameters




### -param pdwFlags [out]

Pointer to a <b>DWORD</b> that receives the current icon display mode for a system language bar item. For more information about possible values, see the dwFlags parameter in <a href="https://msdn.microsoft.com/en-us/library/ms628955(v=VS.85).aspx">ITfSystemDeviceTypeLangBarItem::SetIconMode</a>.


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




<a href="https://msdn.microsoft.com/en-us/library/ms628953(v=VS.85).aspx">ITfSystemDeviceTypeLangBarItem</a>



<a href="https://msdn.microsoft.com/25124539-4bf9-4299-b441-9a5fac18b60d">ITfSystemDeviceTypeLangBarItem::SetIconMode
      </a>
 

 

