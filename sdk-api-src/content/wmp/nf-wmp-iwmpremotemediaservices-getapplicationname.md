---
UID: NF:wmp.IWMPRemoteMediaServices.GetApplicationName
title: IWMPRemoteMediaServices::GetApplicationName (wmp.h)
description: The GetApplicationName method is called by Windows Media Player to retrieve the name of the program that is hosting the remoted control.
helpviewer_keywords: ["GetApplicationName","GetApplicationName method [Windows Media Player]","GetApplicationName method [Windows Media Player]","IWMPRemoteMediaServices interface","IWMPRemoteMediaServices interface [Windows Media Player]","GetApplicationName method","IWMPRemoteMediaServices.GetApplicationName","IWMPRemoteMediaServices::GetApplicationName","IWMPRemoteMediaServicesGetApplicationName","wmp.iwmpremotemediaservices_getapplicationname","wmp/IWMPRemoteMediaServices::GetApplicationName"]
old-location: wmp\iwmpremotemediaservices_getapplicationname.htm
tech.root: WMP
ms.assetid: b3a210f9-90ea-4a6e-8aab-9e8cd7e21ab6
ms.date: 12/05/2018
ms.keywords: GetApplicationName, GetApplicationName method [Windows Media Player], GetApplicationName method [Windows Media Player],IWMPRemoteMediaServices interface, IWMPRemoteMediaServices interface [Windows Media Player],GetApplicationName method, IWMPRemoteMediaServices.GetApplicationName, IWMPRemoteMediaServices::GetApplicationName, IWMPRemoteMediaServicesGetApplicationName, wmp.iwmpremotemediaservices_getapplicationname, wmp/IWMPRemoteMediaServices::GetApplicationName
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
 - IWMPRemoteMediaServices::GetApplicationName
 - wmp/IWMPRemoteMediaServices::GetApplicationName
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
 - IWMPRemoteMediaServices.GetApplicationName
---

# IWMPRemoteMediaServices::GetApplicationName


## -description

The <b>GetApplicationName</b> method is called by Windows Media Player to retrieve the name of the program that is hosting the remoted control.

## -parameters

### -param pbstrName [out]

Pointer to a <b>BSTR</b> containing the name of the host program.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>

## -remarks

This method is used only when remoting the Windows Media Player control.

The full mode of Windows Media Player displays the program name on the <b>View</b> menu under <b>Switch to Other Program</b>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices">IWMPRemoteMediaServices Interface</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>