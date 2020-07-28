---
UID: NF:contentpartner.IWMPContentPartner.SetCallback
title: IWMPContentPartner::SetCallback (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","SetCallback method","IWMPContentPartner.SetCallback","IWMPContentPartner::SetCallback","IWMPContentPartnerSetCallback","SetCallback","SetCallback method [Windows Media Player]","SetCallback method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::SetCallback","wmp.iwmpcontentpartner_setcallback"]
old-location: wmp\iwmpcontentpartner_setcallback.htm
tech.root: WMP
ms.assetid: eb3b0c68-b071-476c-ab14-e4ee34bc9044
ms.date: 12/05/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],SetCallback method, IWMPContentPartner.SetCallback, IWMPContentPartner::SetCallback, IWMPContentPartnerSetCallback, SetCallback, SetCallback method [Windows Media Player], SetCallback method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::SetCallback, wmp.iwmpcontentpartner_setcallback
f1_keywords:
- contentpartner/IWMPContentPartner.SetCallback
dev_langs:
- c++
req.header: contentpartner.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- contentpartner.h
api_name:
- IWMPContentPartner.SetCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartner::SetCallback


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>SetCallback</b> method provides the plug-in with a pointer for calling Windows Media Player methods.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback">IWMPContentPartnerCallback</a> interface.


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



Windows Media Player calls this function when instantiating the plug-in to provide the callback pointer. The Player also calls this function during shutdown and passes <b>NULL</b> for the parameter value. This signals the plug-in to release the callback pointer provided by the previous call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>
 

 

