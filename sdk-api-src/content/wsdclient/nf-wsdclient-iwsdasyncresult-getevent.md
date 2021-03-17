---
UID: NF:wsdclient.IWSDAsyncResult.GetEvent
title: IWSDAsyncResult::GetEvent (wsdclient.h)
description: Retrieves a WSD_EVENT structure that contains the result of the event.
helpviewer_keywords: ["GetEvent","GetEvent method","GetEvent method","IWSDAsyncResult interface","IWSDAsyncResult interface","GetEvent method","IWSDAsyncResult.GetEvent","IWSDAsyncResult::GetEvent","ncd.iwsdasyncresult_getevent_method","wsdclient/IWSDAsyncResult::GetEvent"]
old-location: ncd\iwsdasyncresult_getevent_method.htm
tech.root: ncd
ms.assetid: de201c8b-9052-42f9-b95d-3b65cf0c86a3
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method, GetEvent method,IWSDAsyncResult interface, IWSDAsyncResult interface,GetEvent method, IWSDAsyncResult.GetEvent, IWSDAsyncResult::GetEvent, ncd.iwsdasyncresult_getevent_method, wsdclient/IWSDAsyncResult::GetEvent
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDAsyncResult::GetEvent
 - wsdclient/IWSDAsyncResult::GetEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDAsyncResult.GetEvent
---

# IWSDAsyncResult::GetEvent


## -description

Retrieves a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure that contains the result of the event.

## -parameters

### -param pEvent [out]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_event">WSD_EVENT</a> structure that provides data about the event.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pEvent</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Event is not yet available or the asynchronous operation has not completed.

</td>
</tr>
</table>

## -remarks

This method should only be called by <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a> and only after the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a> object has signaled that the operation has completed.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdasyncresult">IWSDAsyncResult</a>