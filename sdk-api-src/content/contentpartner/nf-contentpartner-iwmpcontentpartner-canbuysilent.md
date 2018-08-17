---
UID: NF:contentpartner.IWMPContentPartner.CanBuySilent
title: IWMPContentPartner::CanBuySilent
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_canbuysilent.htm
old-project: WMP
ms.assetid: 1faec369-199e-48d4-9c0a-6cbad39a7073
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CanBuySilent, CanBuySilent method [Windows Media Player], CanBuySilent method [Windows Media Player],IWMPContentPartner interface, IWMPContentPartner interface [Windows Media Player],CanBuySilent method, IWMPContentPartner.CanBuySilent, IWMPContentPartner::CanBuySilent, IWMPContentPartnerCanBuySilent, contentpartner/IWMPContentPartner::CanBuySilent, wmp.iwmpcontentpartner_canbuysilent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: contentpartner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
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
tech.root: 
req.typenames: WMPTransactionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.CanBuySilent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWMPContentPartner::CanBuySilent


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>CanBuySilent</b> method calculates the total price of a purchase and determines whether the purchase can proceed without displaying a dialog box.




## -parameters




### -param pInfo [in]

Pointer to a content container list that represents the content to be purchased.


### -param pbstrTotalPrice [out]

Pointer to a <b>BSTR</b> that receives the total price.


### -param pSilentOK [out]

Receives VARIANT_TRUE if the purchase can proceed silently; that is, without displaying a dialog box. Otherwise it receives VARIANT_FALSE.


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



The format of the string returned in <i>pbstrTotalPrice</i> is known only to the online store. Windows Media Player displays, but does not interpret, price strings. For more information about how Windows Media Player and the content partner plug-in exchange price information, see <a href="https://msdn.microsoft.com/en-us/library/Dd564215(v=VS.85).aspx">Purchasing Media Content</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563141(v=VS.85).aspx">IWMPContentPartner Interface</a>
 

 

