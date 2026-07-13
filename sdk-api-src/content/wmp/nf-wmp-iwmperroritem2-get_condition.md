---
UID: NF:wmp.IWMPErrorItem2.get_condition
title: IWMPErrorItem2::get_condition (wmp.h)
description: The get_condition method retrieves a value indicating the condition for the error.
helpviewer_keywords: ["IWMPErrorItem2 interface [Windows Media Player]","get_condition method","IWMPErrorItem2.get_condition","IWMPErrorItem2::get_condition","IWMPErrorItem2get_condition","get_condition","get_condition method [Windows Media Player]","get_condition method [Windows Media Player]","IWMPErrorItem2 interface","wmp.iwmperroritem2_get_condition","wmp/IWMPErrorItem2::get_condition"]
old-location: wmp\iwmperroritem2_get_condition.htm
tech.root: WMP
ms.assetid: fe72bb1c-78ac-4a10-9abf-81722139d842
ms.date: 4/26/2023
ms.keywords: IWMPErrorItem2 interface [Windows Media Player],get_condition method, IWMPErrorItem2.get_condition, IWMPErrorItem2::get_condition, IWMPErrorItem2get_condition, get_condition, get_condition method [Windows Media Player], get_condition method [Windows Media Player],IWMPErrorItem2 interface, wmp.iwmperroritem2_get_condition, wmp/IWMPErrorItem2::get_condition
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPErrorItem2::get_condition
 - wmp/IWMPErrorItem2::get_condition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPErrorItem2.get_condition
---

# IWMPErrorItem2::get_condition


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_condition</b> method retrieves a value indicating the condition for the error.

## -parameters

### -param plCondition [out]

Pointer to a <b>long</b> containing the condition code.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.

<b>Windows Media Player 10 Mobile: </b>This method always retrieves a <b>long</b> set to 0.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperroritem2">IWMPErrorItem2 Interface</a>