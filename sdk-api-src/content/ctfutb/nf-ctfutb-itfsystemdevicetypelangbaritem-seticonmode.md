---
UID: NF:ctfutb.ITfSystemDeviceTypeLangBarItem.SetIconMode
title: ITfSystemDeviceTypeLangBarItem::SetIconMode (ctfutb.h)
description: ITfSystemDeviceTypeLangBarItem::SetIconMode method
helpviewer_keywords: ["0","ITfSystemDeviceTypeLangBarItem interface [Text Services Framework]","SetIconMode method","ITfSystemDeviceTypeLangBarItem.SetIconMode","ITfSystemDeviceTypeLangBarItem::SetIconMode","SetIconMode","SetIconMode method [Text Services Framework]","SetIconMode method [Text Services Framework]","ITfSystemDeviceTypeLangBarItem interface","TF_DTLBI_USEPROFILEICON","_tsf_itfsystemdevicetypelangbaritem_seticonmode_ref","ctfutb/ITfSystemDeviceTypeLangBarItem::SetIconMode","tsf.itfsystemdevicetypelangbaritem_seticonmode"]
old-location: tsf\itfsystemdevicetypelangbaritem_seticonmode.htm
tech.root: TSF
ms.assetid: 25124539-4bf9-4299-b441-9a5fac18b60d
ms.date: 12/05/2018
ms.keywords: 0, ITfSystemDeviceTypeLangBarItem interface [Text Services Framework],SetIconMode method, ITfSystemDeviceTypeLangBarItem.SetIconMode, ITfSystemDeviceTypeLangBarItem::SetIconMode, SetIconMode, SetIconMode method [Text Services Framework], SetIconMode method [Text Services Framework],ITfSystemDeviceTypeLangBarItem interface, TF_DTLBI_USEPROFILEICON, _tsf_itfsystemdevicetypelangbaritem_seticonmode_ref, ctfutb/ITfSystemDeviceTypeLangBarItem::SetIconMode, tsf.itfsystemdevicetypelangbaritem_seticonmode
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
 - ITfSystemDeviceTypeLangBarItem::SetIconMode
 - ctfutb/ITfSystemDeviceTypeLangBarItem::SetIconMode
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
 - ITfSystemDeviceTypeLangBarItem.SetIconMode
---

# ITfSystemDeviceTypeLangBarItem::SetIconMode


## -description

Modifies the type of icon displayed for a system language bar item.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemdevicetypelangbaritem">ITfSystemDeviceTypeLangBarItem</a>



<a href="/windows/desktop/TSF/miscellaneous-language-bar-constants">Miscellaneous Language Bar Constants</a>