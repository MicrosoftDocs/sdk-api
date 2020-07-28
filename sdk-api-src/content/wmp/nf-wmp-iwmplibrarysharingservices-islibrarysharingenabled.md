---
UID: NF:wmp.IWMPLibrarySharingServices.isLibrarySharingEnabled
title: IWMPLibrarySharingServices::isLibrarySharingEnabled (wmp.h)
description: The isLibrarySharingEnabled method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.
helpviewer_keywords: ["IWMPLibrarySharingServices interface [Windows Media Player]","isLibrarySharingEnabled method","IWMPLibrarySharingServices.isLibrarySharingEnabled","IWMPLibrarySharingServices::isLibrarySharingEnabled","IWMPLibrarySharingServicesisLibrarySharingEnabled","isLibrarySharingEnabled","isLibrarySharingEnabled method [Windows Media Player]","isLibrarySharingEnabled method [Windows Media Player]","IWMPLibrarySharingServices interface","wmp.iwmplibrarysharingservices_islibrarysharingenabled","wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled"]
old-location: wmp\iwmplibrarysharingservices_islibrarysharingenabled.htm
tech.root: WMP
ms.assetid: bd643869-9111-423e-9f9c-7147d1e3c7b8
ms.date: 12/05/2018
ms.keywords: IWMPLibrarySharingServices interface [Windows Media Player],isLibrarySharingEnabled method, IWMPLibrarySharingServices.isLibrarySharingEnabled, IWMPLibrarySharingServices::isLibrarySharingEnabled, IWMPLibrarySharingServicesisLibrarySharingEnabled, isLibrarySharingEnabled, isLibrarySharingEnabled method [Windows Media Player], isLibrarySharingEnabled method [Windows Media Player],IWMPLibrarySharingServices interface, wmp.iwmplibrarysharingservices_islibrarysharingenabled, wmp/IWMPLibrarySharingServices::isLibrarySharingEnabled
f1_keywords:
- wmp/IWMPLibrarySharingServices.isLibrarySharingEnabled
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.dll
api_name:
- IWMPLibrarySharingServices.isLibrarySharingEnabled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPLibrarySharingServices::isLibrarySharingEnabled


## -description



The <b>isLibrarySharingEnabled</b> method retrieves a value indicating whether the user has enabled library sharing in Windows Media Player.




## -parameters




### -param pvbEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives the result. <b>VARIANT_TRUE</b> indicates that the user has enabled library sharing.


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



<b>Windows Media Player 10 Mobile:</b> This method is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices">IWMPLibrarySharingServices Interface</a>
 

 

