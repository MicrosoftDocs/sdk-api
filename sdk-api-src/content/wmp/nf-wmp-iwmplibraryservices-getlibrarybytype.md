---
UID: NF:wmp.IWMPLibraryServices.getLibraryByType
title: IWMPLibraryServices::getLibraryByType (wmp.h)
description: The getLibraryByType method retrieves a pointer to an IWMPLibrary interface that represents the library that has the specified type and index.
helpviewer_keywords: ["IWMPLibraryServices interface [Windows Media Player]","getLibraryByType method","IWMPLibraryServices.getLibraryByType","IWMPLibraryServices::getLibraryByType","IWMPLibraryServicesgetLibraryByType","getLibraryByType","getLibraryByType method [Windows Media Player]","getLibraryByType method [Windows Media Player]","IWMPLibraryServices interface","wmp.iwmplibraryservices_getlibrarybytype","wmp/IWMPLibraryServices::getLibraryByType"]
old-location: wmp\iwmplibraryservices_getlibrarybytype.htm
tech.root: WMP
ms.assetid: 766cfd4e-53e6-44a8-87e6-2b9c1fa2ff3f
ms.date: 4/26/2023
ms.keywords: IWMPLibraryServices interface [Windows Media Player],getLibraryByType method, IWMPLibraryServices.getLibraryByType, IWMPLibraryServices::getLibraryByType, IWMPLibraryServicesgetLibraryByType, getLibraryByType, getLibraryByType method [Windows Media Player], getLibraryByType method [Windows Media Player],IWMPLibraryServices interface, wmp.iwmplibraryservices_getlibrarybytype, wmp/IWMPLibraryServices::getLibraryByType
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
 - IWMPLibraryServices::getLibraryByType
 - wmp/IWMPLibraryServices::getLibraryByType
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
 - IWMPLibraryServices.getLibraryByType
---

# IWMPLibraryServices::getLibraryByType


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>getLibraryByType</b> method retrieves a pointer to an <b>IWMPLibrary</b> interface that represents the library that has the specified type and index.

## -parameters

### -param wmplt [in]

<b>WMPLibraryType</b> enumeration value that specifies the type of library to retrieve.

### -param lIndex [in]

A <b>long</b> containing the index of the library to retrieve.

### -param ppIWMPLibrary [out]

Address of a variable that receives a pointer to the retrieved <b>IWMPLibrary</b> interface.

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

There is only one local library and disc libraries are available only on data CDs and DVDs that contain media content.

<b>Windows Media Player 10 Mobile:</b> This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices">IWMPLibraryServices Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmplibrarytype">WMPLibraryType</a>