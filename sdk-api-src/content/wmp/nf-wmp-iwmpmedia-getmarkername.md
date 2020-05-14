---
UID: NF:wmp.IWMPMedia.getMarkerName
title: IWMPMedia::getMarkerName (wmp.h)
description: The getMarkerName method retrieves the name of the marker at the specified index.helpviewer_keywords: ["IWMPMedia interface [Windows Media Player]","getMarkerName method","IWMPMedia.getMarkerName","IWMPMedia2 interface [Windows Media Player]","getMarkerName method","IWMPMedia2::getMarkerName","IWMPMedia3 interface [Windows Media Player]","getMarkerName method","IWMPMedia3::getMarkerName","IWMPMedia::getMarkerName","IWMPMediagetMarkerName","getMarkerName","getMarkerName method [Windows Media Player]","getMarkerName method [Windows Media Player]","IWMPMedia interface","getMarkerName method [Windows Media Player]","IWMPMedia2 interface","getMarkerName method [Windows Media Player]","IWMPMedia3 interface","wmp.iwmpmedia_getmarkername","wmp/IWMPMedia2::getMarkerName","wmp/IWMPMedia3::getMarkerName","wmp/IWMPMedia::getMarkerName"]
old-location: wmp\iwmpmedia_getmarkername.htm
tech.root: WMP
ms.assetid: 86c3931f-5790-43f5-896d-1728c38247a9
ms.date: 12/05/2018
ms.keywords: IWMPMedia interface [Windows Media Player],getMarkerName method, IWMPMedia.getMarkerName, IWMPMedia2 interface [Windows Media Player],getMarkerName method, IWMPMedia2::getMarkerName, IWMPMedia3 interface [Windows Media Player],getMarkerName method, IWMPMedia3::getMarkerName, IWMPMedia::getMarkerName, IWMPMediagetMarkerName, getMarkerName, getMarkerName method [Windows Media Player], getMarkerName method [Windows Media Player],IWMPMedia interface, getMarkerName method [Windows Media Player],IWMPMedia2 interface, getMarkerName method [Windows Media Player],IWMPMedia3 interface, wmp.iwmpmedia_getmarkername, wmp/IWMPMedia2::getMarkerName, wmp/IWMPMedia3::getMarkerName, wmp/IWMPMedia::getMarkerName
f1_keywords:
- wmp/IWMPMedia.getMarkerName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPMedia.getMarkerName
- IWMPMedia2.getMarkerName
- IWMPMedia3.getMarkerName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPMedia::getMarkerName


## -description



The <b>getMarkerName</b> method retrieves the name of the marker at the specified index.




## -parameters




### -param MarkerNum [in]

<b>long</b> specifying the marker index.


### -param pbstrMarkerName [out]

Pointer to a <b>BSTR</b> containing the marker name.


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



This method returns <b>NULL</b> if the specified marker does not exist.

Some media items do not contain markers. Use <b>get_markerCount</b> to find out how many markers are in the current media item.

Marker index numbers start at 1.

Before calling this method, you must have read access to the library. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMP/library-access">Library Access</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_markercount">IWMPMedia::get_markerCount</a>
 

 

