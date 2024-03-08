---
UID: NF:wmp.IWMPLibraryServices.getCountByType
title: IWMPLibraryServices::getCountByType (wmp.h)
description: The getCountByType method retrieves the count of available libraries of a specified type.
helpviewer_keywords: ["IWMPLibraryServices interface [Windows Media Player]","getCountByType method","IWMPLibraryServices.getCountByType","IWMPLibraryServices::getCountByType","IWMPLibraryServicesgetCountByType","getCountByType","getCountByType method [Windows Media Player]","getCountByType method [Windows Media Player]","IWMPLibraryServices interface","wmp.iwmplibraryservices_getcountbytype","wmp/IWMPLibraryServices::getCountByType"]
old-location: wmp\iwmplibraryservices_getcountbytype.htm
tech.root: WMP
ms.assetid: e592fc2e-97d8-4d3c-bbef-7cbaa63a6909
ms.date: 4/26/2023
ms.keywords: IWMPLibraryServices interface [Windows Media Player],getCountByType method, IWMPLibraryServices.getCountByType, IWMPLibraryServices::getCountByType, IWMPLibraryServicesgetCountByType, getCountByType, getCountByType method [Windows Media Player], getCountByType method [Windows Media Player],IWMPLibraryServices interface, wmp.iwmplibraryservices_getcountbytype, wmp/IWMPLibraryServices::getCountByType
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
 - IWMPLibraryServices::getCountByType
 - wmp/IWMPLibraryServices::getCountByType
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
 - IWMPLibraryServices.getCountByType
---

# IWMPLibraryServices::getCountByType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getCountByType</b> method retrieves the count of available libraries of a specified type.

## -parameters

### -param wmplt [in]

<a href="/windows/desktop/api/wmp/ne-wmp-wmplibrarytype">WMPLibraryType</a> enumeration value that specifies the type of library to count.

### -param plCount [out]

Pointer to a <b>long</b> that receives the library count.

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

To obtain a count of the libraries represented by the wmpltRemote value of the <b>WMPLibraryType</b> enumeration, the Player control must be running in remote mode. For information about running the Player control in remote mode, see <a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.

You must initialize the <i>plCount</i> variable before passing in its pointer.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices">IWMPLibraryServices Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmplibrarytype">WMPLibraryType</a>