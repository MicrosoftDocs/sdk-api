---
UID: NF:wmp.IWMPCdromBurn.getItemInfo
title: IWMPCdromBurn::getItemInfo (wmp.h)
description: The getItemInfo method retrieves the value of the specified attribute for the CD.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","getItemInfo method","IWMPCdromBurn.getItemInfo","IWMPCdromBurn::getItemInfo","IWMPCdromBurngetItemInfo","getItemInfo","getItemInfo method [Windows Media Player]","getItemInfo method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_getiteminfo","wmp/IWMPCdromBurn::getItemInfo"]
old-location: wmp\iwmpcdromburn_getiteminfo.htm
tech.root: WMP
ms.assetid: f54b406f-0441-4ed3-8f8b-6794ab2180d9
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],getItemInfo method, IWMPCdromBurn.getItemInfo, IWMPCdromBurn::getItemInfo, IWMPCdromBurngetItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_getiteminfo, wmp/IWMPCdromBurn::getItemInfo
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn::getItemInfo
 - wmp/IWMPCdromBurn::getItemInfo
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
 - IWMPCdromBurn.getItemInfo
---

# IWMPCdromBurn::getItemInfo


## -description

The <b>getItemInfo</b> method retrieves the value of the specified attribute for the CD.

## -parameters

### -param bstrItem [in]

<b>BSTR</b> that contains one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AvailableTime</td>
<td>Retrieves the time available on the CD, in seconds.</td>
</tr>
<tr>
<td>Blank</td>
<td>Retrieves a <b>Boolean</b> (represented as a string) indicating whether the CD is blank.</td>
</tr>
<tr>
<td>FreeSpace</td>
<td>Retrieves the free space on the CD, in bytes.</td>
</tr>
<tr>
<td>TotalSpace</td>
<td>Retrieves the total space on the CD, in bytes.</td>
</tr>
</table>

### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that receives the returned value.

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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>