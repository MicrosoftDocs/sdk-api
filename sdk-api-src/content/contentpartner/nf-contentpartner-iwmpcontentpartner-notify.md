---
UID: NF:contentpartner.IWMPContentPartner.Notify
title: IWMPContentPartner::Notify
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_notify.htm
tech.root: WMP
ms.assetid: 9464ce82-cd84-4a35-83d2-e46198c0c1e7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],Notify method, IWMPContentPartner.Notify, IWMPContentPartner::Notify, IWMPContentPartnerNotify, Notify, Notify method [Windows Media Player], Notify method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::Notify, wmp.iwmpcontentpartner_notify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMPContentPartner.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPContentPartner::Notify


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Notify</b> method provides the content partner plug-in with event notifications from Windows Media Player.




## -parameters




### -param type [in]

The notification type, specified as a member of the <a href="https://msdn.microsoft.com/a9292277-5283-41b8-86a6-f7059aa38a69">WMPPartnerNotification</a> enumeration.


### -param pContext [in]

Pointer to a <b>VARIANT</b> that contains notification data.


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



The data type for <i>pContext</i> is <b>VT_EMPTY</b> for all notifications except wmpsnCatalogDownloadFailure. In the case of a catalog download failure, the data type is <b>VT_ERROR</b> and the variable contains an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/a9292277-5283-41b8-86a6-f7059aa38a69">WMPPartnerNotification</a>
 

 

