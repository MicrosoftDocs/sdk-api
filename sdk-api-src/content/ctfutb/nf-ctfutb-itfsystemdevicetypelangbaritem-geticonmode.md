---
UID: NF:ctfutb.ITfSystemDeviceTypeLangBarItem.GetIconMode
title: ITfSystemDeviceTypeLangBarItem::GetIconMode (ctfutb.h)
description: ITfSystemDeviceTypeLangBarItem::GetIconMode method
helpviewer_keywords: ["GetIconMode","GetIconMode method [Text Services Framework]","GetIconMode method [Text Services Framework]","ITfSystemDeviceTypeLangBarItem interface","ITfSystemDeviceTypeLangBarItem interface [Text Services Framework]","GetIconMode method","ITfSystemDeviceTypeLangBarItem.GetIconMode","ITfSystemDeviceTypeLangBarItem::GetIconMode","_tsf_itfsystemdevicetypelangbaritem_geticonmode_ref","ctfutb/ITfSystemDeviceTypeLangBarItem::GetIconMode","tsf.itfsystemdevicetypelangbaritem_geticonmode"]
old-location: tsf\itfsystemdevicetypelangbaritem_geticonmode.htm
tech.root: TSF
ms.assetid: 0ac293de-0a35-4b3a-98af-f47849fd7149
ms.date: 12/05/2018
ms.keywords: GetIconMode, GetIconMode method [Text Services Framework], GetIconMode method [Text Services Framework],ITfSystemDeviceTypeLangBarItem interface, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],GetIconMode method, ITfSystemDeviceTypeLangBarItem.GetIconMode, ITfSystemDeviceTypeLangBarItem::GetIconMode, _tsf_itfsystemdevicetypelangbaritem_geticonmode_ref, ctfutb/ITfSystemDeviceTypeLangBarItem::GetIconMode, tsf.itfsystemdevicetypelangbaritem_geticonmode
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfSystemDeviceTypeLangBarItem::GetIconMode
 - ctfutb/ITfSystemDeviceTypeLangBarItem::GetIconMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSystemDeviceTypeLangBarItem.GetIconMode
---

# ITfSystemDeviceTypeLangBarItem::GetIconMode


## -description

Obtains the current icon display mode for a system language bar item.

## -parameters

### -param pdwFlags [out]

Pointer to a <b>DWORD</b> that receives the current icon display mode for a system language bar item. For more information about possible values, see the dwFlags parameter in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode">ITfSystemDeviceTypeLangBarItem::SetIconMode</a>.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemdevicetypelangbaritem">ITfSystemDeviceTypeLangBarItem</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode">ITfSystemDeviceTypeLangBarItem::SetIconMode
      </a>