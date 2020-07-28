---
UID: NF:wmp.IWMPLibrary2.getItemInfo
title: IWMPLibrary2::getItemInfo (wmp.h)
description: The getItemInfo method retrieves the value of the LibraryID attribute.
helpviewer_keywords: ["IWMPLibrary2 interface [Windows Media Player]","getItemInfo method","IWMPLibrary2.getItemInfo","IWMPLibrary2::getItemInfo","getItemInfo","getItemInfo method [Windows Media Player]","getItemInfo method [Windows Media Player]","IWMPLibrary2 interface","wmp.iwmplibrary2_getiteminfo","wmp/IWMPLibrary2::getItemInfo"]
old-location: wmp\iwmplibrary2_getiteminfo.htm
tech.root: WMP
ms.assetid: 38de9e72-b942-4c09-be9e-ff9f345c778d
ms.date: 12/05/2018
ms.keywords: IWMPLibrary2 interface [Windows Media Player],getItemInfo method, IWMPLibrary2.getItemInfo, IWMPLibrary2::getItemInfo, getItemInfo, getItemInfo method [Windows Media Player], getItemInfo method [Windows Media Player],IWMPLibrary2 interface, wmp.iwmplibrary2_getiteminfo, wmp/IWMPLibrary2::getItemInfo
f1_keywords:
- wmp/IWMPLibrary2.getItemInfo
dev_langs:
- c++
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.h
api_name:
- IWMPLibrary2.getItemInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPLibrary2::getItemInfo


## -description


The <b>getItemInfo</b> method retrieves the value of the <b>LibraryID</b> attribute.


## -parameters




### -param bstrItemName [in]

<b>BSTR</b> containing the attribute name. Set the value of this parameter to "LibraryID".


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that receives the value of the <b>LibraryID</b> attribute.


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



The <b>LibraryID</b> attribute retrieved by this method is the same as the <b>LibraryID</b> attribute that <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo">IWMPMedia::getItemInfo</a> retrieves for each media item in the library.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmplibrary2">IWMPLibrary2</a>
 

 

